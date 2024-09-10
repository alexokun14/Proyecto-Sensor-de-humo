<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sensor de Humo</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: url('data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxISEhMSEhASFhUQFRIVFRUWFRAPFg8VFRUWFhUXFxYYHSggGBolGxUVITEhJSkrLi4uFx8zODMtNygtLisBCgoKDg0OGhAQGi0lIB8tLS0rKystLS0rLS0tLS0tLS0tKy0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tKy01LS0rL//AABEIALsBDgMBIgACEQEDEQH/xAAcAAABBQEBAQAAAAAAAAAAAAAAAQIDBAUGBwj/xABAEAACAQIDBQYCCAMGBwAAAAABAgADEQQSIQUxQVFhBhMicYGRMqEHFCNCUpKxwWKC0URTcqKy8BUkM0Nj4fH/xAAaAQEAAwEBAQAAAAAAAAAAAAAAAQIDBAUG/8QAKBEBAQACAgICAAQHAAAAAAAAAAECEQMhEjEEQQUiUWETMjNCobHw/9oADAMBAAIRAxEAPwDw/MeZj6dQg3kYlnDYdqhyqpMi1fjlt69lr1ww3WPOV8x5zTxOxqiKGawvJtg9mcRi2+yWyA2ao1wi+R+8eglcbL6ac2GeN/PNMbMeZmls7ZOJxFjSouw5/Cv5jYT0zYvYXDULF175/wATgZQelPd73nULhdNBpw4AeUtVMZa8pw3YKu2tSqidBmqH9hNGl2DpD4qtU+qID8jPQDQkRoyEacWex2H/AAt+d5Ur9jqJ3M48mv8AqDO6ejK9XDyLtOnnuI7HH7lY/wAwv+lpl4nsxik1C5wPwtc+x19p6XUoxqpI8qeMePNcEg3uNCDcWjcx5met47s5h8TfvEs5/wC4tle/Xg3rOF7SdkK+E8du8o8Kqg+Ho6/cPy6y0ylVuNjnrnmYtzzMQQJlkdDMeZhc8zEgTCC5jzMMx5mNhAXMeZhmPMxIQFzHmYZjzMSEBcx5mGY8zEhAXMeZhmPMxIQFzHmYuY8zGxYC5jzMMx5mJCAuY8zDMeZiQgSIs1dm16gbwC0qYFbMNL34T03sTsWliTbJ9nSy942ozE7kB5njyHmJhyZfWnqfE4f7rlrTL7N9knxrCtiSwogmwuQa5G+3JOvtznpWHwaoqqihVUWCqAAo6ATafAqBZQAFAAA0AA3ASsaVpfD1pz/Ixvl5VS7qOKG0uKknNAGTazwxt9VjmjGNRmq+EMb9UHEyWd6uqyWpStVpToRhF6+8RsAh4fMyFo5KrRkJpzq6mzKZ+6fcyu+xk4Mw9jIsNsOgk2cIgYFWAKsCGBAYMDvBB3iNOyWXcQw9jJsKhBsQQesqmx5J9JPYv6mwr0Afq9U2tqfq778hP4TrY9COGvCz6i2nstcXh6uGfdXQqD+Ft6N6MAfSfMWIoMjMjCzISrA71ZTYj3E1lY2IoQiyUEhFtC0BIRYQCJHRISIQEIBCEIBCESEFhCEAhEhA6HY+ENSoqKLs5Cr5k2H6z6A7P7DTC0adFNcguzf3jn429T8rTzT6L9i58ZTe2lFXqHqQMq/NgfSe30sPYTl8nrcn5dY1W7k2kD4e81whAkZpSZlpjll5RljC23yVEtLhpxhpzTe1McdKrJISkuMLSBiL2JAJ3C4ufSWjPPHdQlY0iTMJlYnbNFHNNm8SmxF1Gtr8T1ks10rGZZAm0UO7NboM36XklPEIdzDyOn6wWpMsdkvASamJCvkWjTtungn0u7LFDaVVgLLiVWuOV3uH/wA6t7z6BRZ5r9POy8+Gw+KA1o1GpP8A4agzKfLMh/NJkPJ4myxMsW8aWkl0W0I28W8I2LQhEJgLeEbHCSiCJAxICxY2LAIkIQgsIkWARIQgfR30WYUCpV01NIW/ML/tPR1QDfrOR7DUEQKwIzVCyH+EBcw9yJ1+YHScXx7vDb1fxG757r11/jpE68oy0h+sOHqDKuWla+pzEEXuBxlg8+G/0l9yubuGETj8d2jr0sS6GmhooTr8IC20bvN1+npNnaW0D8K/CfQtz8hOH22Cx13DcOC+05s+fvWL0fi/H6tym9xFtjttUYlUB1NtL0kHmfiYe0xcF2jqrXosXsgq08wChQylgDcnU6E7zuEkGx6+INqFItbe2gVfNjoP1mvhPo2Zh/zGIIvwpC5HH43H7Tr48rlNuf5PHOK3F3tc6kHgZ499IdDLj3NhaqlJ78/Dkb/TPXnoNbUnz5zKx+xaVUhqlKm5UWBZVcgb7AmbPP1Y8bpVLEEEg8xdbW6j/ek2sDt6ulvtM4/DU8f+Y+L5zuK/ZbDn+z0vRcv6TOxHYyiR4M9M81Oceob+sbVvbW7IbSGJLqPC1MKWQnMLNexU8tDynTClYziex2wMRhcSc2V6dRFQVEJ8PjB8aHVdPMab56RtyulGkDYEmyp7an2ElRUppMf6Qdk/WNl41LfDSNRf8VIioP8ASR6zoMEocBhuIveSbVroMPWH3BSrZieQRrwPjW8SLEkghCEAhCEAhCEAhCEAhCEAhCEAhCEAhCED6H7K4q2Io66ZwPzAr+89Knj2BxAR1f8ACyn2IP7T2IEHUcdZ5vxutx9H+M4a5Mcv1n/f7NaijEFlBI0B4gScBd2/9o1RMbF7RNMNUGtiLjmCQJvlnMO68jHjy5LqDbmGyrnUfDrblwImdhuziuQ9YXB1Cbhz8X9PedMKquoYbmAI/WUcXiraD3kfwMPLybYfJzxx8J1+4Jp01CqBZdwAsF8hKlTEkyuzm+sjdrdOu6dGqwueM7PrVTzkGaQ4rECmAWD2PFUqVPU5QbCUH2kWYrT7pwR92uKVYcyEZd/rLSMMs/LtpvXUFVZ1DP8ACCwBbyB3yQAzEo1mV1DnEAXGlWglb2q0728zNg1NYUW8JVysDDtTTYii6m9OzDyY2P6A+0jD3Eu0Q1SjVpkbhmX/ABLqLQg/YAPcrfm36znvpe2wMLsyqoNqmL+wQdG1qn0QMPNhOzw1JaFEGowVaa3diQAoGrEmfNX0pdq2x+KLrcUaYyUVOlkvq5HBmOp6BRwkyDhSIoWKDzklSsLWAkiJogiRYAREixIBCEIBCEIBCEIBCEIBCEIBCEIHsY4jhPR+xG2hXoCmW+0w4VW5sm5H9hY9R1nmeMeykgzKwPaVsPXp1KJ8aE6HdUU2zK3Q/wDvhPN4N+XT678VmF4vze53H0OtSc9iqOYvTJtmuP6SzsDbNPF0xUpaGwz0zbNSPXmOTDQ/KaFTAhmDbiN/WdfJxeT574/NMaMd4QFHAAeQtMepVOouONuOvCa20xreYtU6y0nauWvGX7UjjGB7t2olujvh3NxcWDXB9DK+JLWs3fWPCpSp4pD/ADJ4veawS62vb0DeljMUmkrZrU1N/wDzYQnzHwmT6qNTKJ6GyFA/u2BNzRarSW3A2zW/aWMTs7MLXRjbTvEWoD57j85OuKDLoDbjltUv+W8QbQTSzLm3ZXJpH0zDfJjOzTBqYMqTlWx1/wCjiXQ34/ZVPDNKi5KglXU7rOFDacTlJGstYhcw8YYr/FTpV1PqusjoYIIQVpUwD+BqqaHjka4vLaZXpLRvNvZldUzO7BEpqSzMbBRzJMoJS5TjO1O2FqsKSE9ymtwbd8/4rchuHqeMnSFH6SO2dTGf8vhwRh76nUNXI4kcE5D1PKcrguywqDM4N51GSmgGXKdPMy5hXJ1YZR6TWYq2vLO0WxhS3Ccw62ns216feq9gGsD4SBZgN9iNVM4jGdl8rFvutqAd/lK2bqduSRYrJNCpgGzbjYdJPVRETXUmPE2xDEkz0jvkMokQhCAQhCAQhCAQhCAQhCAQhCB6Ft3HG2UbgJw1bEHNcGdVtN1encGcjWSxnN8eSR7H4pnlllO+nQ9nu0OIp1EK1WUqdGBII9f2nuPZftzUcZcQit/Gngb1XcfS0+cKD7tZ6B2d2sAoudZbkuUvlEfBx4eSXiznd9V7nidrYWoABXVW4K/2ZN+AvofeQnfYiePbd2sCuovaT9mvpGenamy94g0AcnMo5K+8DobiaYZTKbcvyfj5cWdxeuFE5yi1IBmCu199le9r/wALXAnPU+3mEY+PvaV/xIXX8yX+YE08P2kwb7sTS9yP1En7ZSZa3Fv/AIet7lUNx+AI4/mUy4mGUJlubdSX+ZmbW2/gx/aaXo1/0mVi+2WGTd3j9FUgH1aTIpd/boLAaX0i1KqIMzMFHM/sOM892n24rtph6Crf7zfaMPTcPnMCjtLE1Kq94zsxIuTc2HTgJphNsspY9K2/je+QUqbFUf4/xOvLoOnGc3WAViECkXuc12LGVKDPch2O/edP/snSlciwv8p1YceNm2WVsLXxZNgEVLcZj4za1RDlIzdSbW9J1VbDBk+EAziNut3ZI4iVyn6K43toYTbOjK3wta9tDcftLv8AxOmRrTuOus4mniRe95oris62DaSsx2taXb+PV/BSRV4aAfOc7X7umPF4mmhiQqXInOVwXbzMryddLY9oKtQm/KQzUqYTSw1MznSxtMbFzIRxSNkAhCEAhCEAhCEAhCEAhCEDoKjlVsZiV2uZaxOI0tKJmeGOu3X8nl8uoBNjYNU55jzV2MwQljyk8n8qvxP6sra29ibLObo17G4MftPGGoeglemw4yvFhqNvl/J8+Tr067Zu3VqKEcAHnLOIrKm5hrynHUqfETSFO/HSWvd6Tw3KTu9NeoxYXRvaXtj0ajkA34egmTgtn6Zgxm1s/aXc3vrcEGaY7x9s85M8tY9NbE4BRqul90hw9Fwbrqem+ZuI2hUceEeVv3lmht4UjkLKPxPe58hymmGUc/Nx2dNGlg3zZqjW8z+02cPkIsX3chaYhqU6gzCpqd3KYm09r5AVvYg2nRNSOa99O82hWAQZTccxqZze2MEldbk2YDfz85xqdoHXQEnXnLGH24zfFJwzxvVVyxs9K20sIKSkXuekz6Vdqeus08a+c6TMxasRYzPPHV6Xx/c99ps5AtGY6gUAbnGYOgQwNjOlbBNVCgpM5LlDK6ckmLb3lijsx3GcDSdgeydOwYnzklF0pEU1taLhfs8/0cFiaRGhG6VDOp7RUMzeETncRhim+Z5ReVXhCEqkQhCAQhCAQhCAQhCA+pGyS0Y0iLZT7BEsUwcsrCONQ84s2thlJ2Ub9Y64kbNeII0r5LdOrJxW53meHljD1hmUtuBFxzEjTWcnTXo4zLpeSfXCNxBv13TPxSq1TwsAp5aC/ISymCHBt287gPWaSb6ZzluN3FvCYl9RmsDv/wB8pXxOGHCFOjbQHP5HLL1MgCxUj+Zf6S816X85eybFquhsT4eUv7c2cKgFVNb2DDiCP6ytTwx+JSvUXAIkqVWQkqw6i4IPmOM3mM8dVzZd3cY67NHUGPfZhAvr7Gapqu3AKOdgvsd/tGLj6dLw3LZjqTw9OEp4RXdZwBUAiDIW1mpjqK2uu42PlKuCp7+svrSJ2m2XjKXwtYEcZdxm2aSCysSZnVdnqASZlNhbyMscsYdVcxfaKoRobCZuH2me8DGLjMNlFrzMdZhlvbSSNvHbQ7w3vaZ2PxAIAEomJK2p0IQhKpEIQgEIQgEIQgEIQgSF4wxIQm3YhCEIEWJCAto6II6QtCtUJ3ndNCjjvAFubA8g28a7z85nKZKKd90tN/RqfbYwG1kpa92GbSxO5eenGXMdXFdbqBmGugAuOI04ic8tAySlimpMGRrEco8rOk/wpryaOHqm11NiJJ9da/iy+YVR+0pU8QjG98rHfyPvL31MOt++pjcNbg6/rNZluM7dXdVa9TN94385Uem46/OWKmCKnRtOu4+oipiCuhk9X2jy/RYXFu1NU/Dx6cI/C4qwsdDKnfCOC314S3c9VRo/WdLO2/dIgQw04SnVQrreV6dUnjaLnfskXMRYixlCthjluOEVn13ySnVOovoZS5SrSMx1jJfqJffI+4AmWl1WLLNSiLXlfLIDTEikQgJFiQgEIQgKBCAgYATEhCAQhCAQhCAt4oMbCE7SXEfTvwkEeHMhaZT7WHrNuMiJkbOTH0gCbEye0Wz6OIj1pHeIvdESWi+XUS00jV3qijUYdJaRlbwutr6BgbZTzPSLTYN8QjzgzwNxL4zZnhruKj0cjEHW3r69RLFNrbjoZewWEz21UW3hjYOOl+Mdi6FGkN12J0AOZVHG9vTSXksY2yq5QlddRzlKth7C6nzHES7SrXFr6Rwoo2/Q9dPnLWeSPTCBIi96RNTGbPynTzmdiKJHCZXCxeZSozXJ3xO+MiIiGZrpGrkxBUjQIhEgPqPeMiQgEIQgLEiwgF4EwAjssJkpkIQhAhCEAhCEAhCEAhCLASLCKIEiVyI8Pci17nfykAkqaKTI9L499VcSou4G0lpYpl+9e26ZJljCxuyNccvPKdNyjtAEWYevGLWqrlta9+ZvMSq5HGLQc33y+GVvtTl8cf5Z20EFuJknegixkNLfFqHSdEvTjqekhawz8d2u7p1lKqTchgfa0KZk/eHnKrIqWALgnKdBeVXogaTTSs1viPvKeKO/rIyxmtktU2pcpCyy7TNgY2somel5VGEc8bKLFtCJCA4iCiKIo3SF9G3iQEDJVf/Z') no-repeat center center fixed;
            background-size: cover;
            color: white;
            text-align: center;
        }
        .container {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            height: 100vh;
            background: rgba(0, 0, 0, 0.5); /* Fondo semitransparente */
            padding: 20px;
        }
        h1 {
            font-size: 3em;
            margin: 0;
        }
        h3 {
            font-size: 1.5em;
            margin: 0;
        }
        nav ul {
            list-style-type: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin: 0 10px;
        }
        nav ul li a {
            text-decoration: none;
            color: white;
            padding: 15px 30px;
            border: 2px solid #4CAF50;
            border-radius: 50px;
            transition: background 0.3s, color 0.3s;
            background: linear-gradient(135deg, #6B8E23, #4CAF50);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            font-size: 1.1em;
        }
        nav ul li a:hover {
            background: #4CAF50;
            color: white;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
        }
        ul {
            list-style-type: none;
            padding: 0;
        }
        ul li {
            font-size: 1.2em;
            margin: 10px 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1><center>Sensor de Humo</center></h1>
        <nav>
            <ul>
                <li><a href="file:///C:/Users/alexa/OneDrive/Escritorio/Página%20web%20Grupo%204/Sistemas%20de%20control.html">Sistema de control</a></li>
                <li><a href="file:///C:/Users/alexa/OneDrive/Escritorio/Página%20web%20Grupo%204/Gestion%20de%20riesgo.html">Gestión de riesgo</a></li>
                <li><a href="file:///C:/Users/alexa/OneDrive/Escritorio/Página%20web%20Grupo%204/Programación.html">Programación</a></li>
                <li><a href="file:///C:/Users/alexa/OneDrive/Escritorio/Página%20web%20Grupo%204/Sistema%20eletrico.html">Sistema eléctrico</a></li>
            </ul>
        </nav>
        <h3><center>Sensor de Humo Para los Baños Con Sistemas de Alerta a Coordinación Académica Con Notificación en el Momento de Actuación</center></h3>
        <p>Integrantes</p>
        <ul>
            <li>Angulo Alexander</li>
            <li>Guevara Leddy</li>
            <li>Murcia Daniela</li>
            <li>Rozo Daniela</li>
        </ul>
    </div>
</body>
</html>
