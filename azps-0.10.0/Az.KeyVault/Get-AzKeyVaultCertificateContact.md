---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: e02b60055818d1ed79e93e6853353795e78c5830
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875845"
---
# <span data-ttu-id="6294a-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="6294a-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="6294a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6294a-102">SYNOPSIS</span></span>
<span data-ttu-id="6294a-103">키 자격 증명 모음에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="6294a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6294a-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6294a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6294a-105">DESCRIPTION</span></span>
<span data-ttu-id="6294a-106">**AzKeyVaultCertificateContact** Cmdlet은 Azure key vault의 키 보관소에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-106">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="6294a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6294a-107">EXAMPLES</span></span>

### <span data-ttu-id="6294a-108">예제 1: 모든 인증서 연락처 가져오기</span><span class="sxs-lookup"><span data-stu-id="6294a-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="6294a-109">이 명령은 Contoso 키 자격 증명 모음의 인증서 개체에 대 한 모든 연락처를 가져온 다음 $Contacts 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="6294a-110">변수</span><span class="sxs-lookup"><span data-stu-id="6294a-110">PARAMETERS</span></span>

### <span data-ttu-id="6294a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6294a-111">-DefaultProfile</span></span>
<span data-ttu-id="6294a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6294a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6294a-113">-VaultName</span></span>
<span data-ttu-id="6294a-114">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-114">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6294a-115">CommonParameters</span></span>
<span data-ttu-id="6294a-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6294a-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6294a-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6294a-118">입력</span><span class="sxs-lookup"><span data-stu-id="6294a-118">INPUTS</span></span>

### <span data-ttu-id="6294a-119">않아야</span><span class="sxs-lookup"><span data-stu-id="6294a-119">None</span></span>
<span data-ttu-id="6294a-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6294a-121">출력</span><span class="sxs-lookup"><span data-stu-id="6294a-121">OUTPUTS</span></span>

### <span data-ttu-id="6294a-122"><를 나열 합니다. KeyVault. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="6294a-122">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="6294a-123">상속자</span><span class="sxs-lookup"><span data-stu-id="6294a-123">NOTES</span></span>

## <span data-ttu-id="6294a-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6294a-124">RELATED LINKS</span></span>

[<span data-ttu-id="6294a-125">추가-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="6294a-125">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="6294a-126">제거-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="6294a-126">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

