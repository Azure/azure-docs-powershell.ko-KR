---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: cf60626ec04a2466fc9565aef5daff896281345d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702370"
---
# <span data-ttu-id="a0673-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a0673-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="a0673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0673-102">SYNOPSIS</span></span>
<span data-ttu-id="a0673-103">키 자격 증명 모음에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0673-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0673-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0673-104">SYNTAX</span></span>

### <span data-ttu-id="a0673-105">VaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a0673-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0673-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a0673-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0673-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0673-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0673-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a0673-108">DESCRIPTION</span></span>
<span data-ttu-id="a0673-109">**AzureKeyVaultCertificateContact** Cmdlet은 Azure key vault의 키 보관소에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0673-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a0673-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a0673-110">EXAMPLES</span></span>

### <span data-ttu-id="a0673-111">예제 1: 모든 인증서 연락처 가져오기</span><span class="sxs-lookup"><span data-stu-id="a0673-111">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="a0673-112">이 명령은 Contoso 키 자격 증명 모음의 인증서 개체에 대 한 모든 연락처를 가져온 다음 $Contacts 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0673-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="a0673-113">변수</span><span class="sxs-lookup"><span data-stu-id="a0673-113">PARAMETERS</span></span>

### <span data-ttu-id="a0673-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0673-114">-DefaultProfile</span></span>
<span data-ttu-id="a0673-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a0673-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0673-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0673-116">-InputObject</span></span>
<span data-ttu-id="a0673-117">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="a0673-117">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0673-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0673-118">-ResourceId</span></span>
<span data-ttu-id="a0673-119">KeyVault Id.</span><span class="sxs-lookup"><span data-stu-id="a0673-119">KeyVault Id.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0673-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a0673-120">-VaultName</span></span>
<span data-ttu-id="a0673-121">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0673-121">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0673-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0673-122">CommonParameters</span></span>
<span data-ttu-id="a0673-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0673-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0673-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0673-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0673-125">입력</span><span class="sxs-lookup"><span data-stu-id="a0673-125">INPUTS</span></span>

### <span data-ttu-id="a0673-126">않아야</span><span class="sxs-lookup"><span data-stu-id="a0673-126">None</span></span>
<span data-ttu-id="a0673-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0673-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0673-128">출력</span><span class="sxs-lookup"><span data-stu-id="a0673-128">OUTPUTS</span></span>

### <span data-ttu-id="a0673-129"><를 나열 합니다. KeyVault. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="a0673-129">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="a0673-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a0673-130">NOTES</span></span>

## <span data-ttu-id="a0673-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0673-131">RELATED LINKS</span></span>

[<span data-ttu-id="a0673-132">추가-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a0673-132">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="a0673-133">제거-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a0673-133">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

