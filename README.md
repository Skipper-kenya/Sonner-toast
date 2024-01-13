# Sonner-toast
#what is sonner? 

it is a toast component for React.

#what is sonner used for? 

tired of using alerts in your website? , sonner with three easy steps provides an amazing alert notifications.

#installation? 

npm install sonner


#USAGE? 

Render the toaster in the root of your app.
import { Toaster, toast } from 'sonner'

// ...

function App() {
  return (
    <div>
      <Toaster />
      <button onClick={() => toast('My first toast')}>
        Give me a toast
      </button>
    </div>
  )
}


#TYPES
toast.success('my success message')
tost.error('error message')
toat.info('info message')
toast.message('Event has been created', {
  description: 'Monday, January 3rd at 6:00pm',
})
toast.warning('Event start time cannot be earlier than 8am')
toast('Event has been created', {
  action: {
    label: 'Undo',
    onClick: () => console.log('Undo')
  },
})
const promise = () => new Promise((resolve) => setTimeout(() => resolve({ name: 'Sonner' }), 2000));
toast.promise(promise, {
  loading: 'Loading...',
  success: (data) => {
    return `${data.name} toast has been added`;
  },
  error: 'Error',
});
