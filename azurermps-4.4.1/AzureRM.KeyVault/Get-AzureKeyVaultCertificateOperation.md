---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: dd9260fa833a09736aaba4b63f56f5b5c894662d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527556"
---
# <span data-ttu-id="6f813-101">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6f813-101">Get-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="6f813-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f813-102">SYNOPSIS</span></span>
<span data-ttu-id="6f813-103">인증서 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f813-103">Gets the status of a certificate operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f813-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f813-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f813-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6f813-105">DESCRIPTION</span></span>
<span data-ttu-id="6f813-106">**Get-AzureKeyVaultCertificateOperation** cmdlet은 인증서 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f813-106">The **Get-AzureKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="6f813-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6f813-107">EXAMPLES</span></span>

### <span data-ttu-id="6f813-108">예제 1: 인증서 작업 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="6f813-108">Example 1: Get the status of a certificate operation</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="6f813-109">이 명령은 ContosoKV01 키 자격 증명 모음에 대 한 TestCert01에 대 한 인증서 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f813-109">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="6f813-110">변수</span><span class="sxs-lookup"><span data-stu-id="6f813-110">PARAMETERS</span></span>

### <span data-ttu-id="6f813-111">-이름</span><span class="sxs-lookup"><span data-stu-id="6f813-111">-Name</span></span>
<span data-ttu-id="6f813-112">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f813-112">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f813-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6f813-113">-VaultName</span></span>
<span data-ttu-id="6f813-114">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f813-114">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f813-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f813-115">-DefaultProfile</span></span>
<span data-ttu-id="6f813-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f813-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f813-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f813-117">CommonParameters</span></span>
<span data-ttu-id="6f813-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f813-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f813-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f813-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f813-120">입력</span><span class="sxs-lookup"><span data-stu-id="6f813-120">INPUTS</span></span>

## <span data-ttu-id="6f813-121">출력</span><span class="sxs-lookup"><span data-stu-id="6f813-121">OUTPUTS</span></span>

### <span data-ttu-id="6f813-122">Microsoft. KeyVault. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6f813-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="6f813-123">상속자</span><span class="sxs-lookup"><span data-stu-id="6f813-123">NOTES</span></span>

## <span data-ttu-id="6f813-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f813-124">RELATED LINKS</span></span>

[<span data-ttu-id="6f813-125">제거-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6f813-125">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="6f813-126">중지-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6f813-126">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

