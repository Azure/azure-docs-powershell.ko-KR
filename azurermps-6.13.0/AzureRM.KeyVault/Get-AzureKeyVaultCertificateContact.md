---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 31619366c1d2a1a025cb7ff563a04b166abb2a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703853"
---
# <span data-ttu-id="2866c-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2866c-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="2866c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2866c-102">SYNOPSIS</span></span>
<span data-ttu-id="2866c-103">키 자격 증명 모음에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2866c-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2866c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2866c-104">SYNTAX</span></span>

### <span data-ttu-id="2866c-105">VaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2866c-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2866c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2866c-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2866c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2866c-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2866c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2866c-108">DESCRIPTION</span></span>
<span data-ttu-id="2866c-109">**AzureKeyVaultCertificateContact** Cmdlet은 Azure key vault의 키 보관소에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2866c-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="2866c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2866c-110">EXAMPLES</span></span>

### <span data-ttu-id="2866c-111">예제 1: 모든 인증서 연락처 가져오기</span><span class="sxs-lookup"><span data-stu-id="2866c-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="2866c-112">이 명령은 Contoso 키 자격 증명 모음의 인증서 개체에 대 한 모든 연락처를 가져온 다음 $Contacts 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2866c-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="2866c-113">변수</span><span class="sxs-lookup"><span data-stu-id="2866c-113">PARAMETERS</span></span>

### <span data-ttu-id="2866c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2866c-114">-DefaultProfile</span></span>
<span data-ttu-id="2866c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2866c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2866c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2866c-116">-InputObject</span></span>
<span data-ttu-id="2866c-117">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="2866c-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2866c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2866c-118">-ResourceId</span></span>
<span data-ttu-id="2866c-119">KeyVault Id.</span><span class="sxs-lookup"><span data-stu-id="2866c-119">KeyVault Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2866c-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2866c-120">-VaultName</span></span>
<span data-ttu-id="2866c-121">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2866c-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2866c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2866c-122">CommonParameters</span></span>
<span data-ttu-id="2866c-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2866c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2866c-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2866c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2866c-125">입력</span><span class="sxs-lookup"><span data-stu-id="2866c-125">INPUTS</span></span>

### <span data-ttu-id="2866c-126">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="2866c-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="2866c-127">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2866c-127">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2866c-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2866c-128">System.String</span></span>

## <span data-ttu-id="2866c-129">출력</span><span class="sxs-lookup"><span data-stu-id="2866c-129">OUTPUTS</span></span>

### <span data-ttu-id="2866c-130">Microsoft. KeyVault. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2866c-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="2866c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="2866c-131">NOTES</span></span>

## <span data-ttu-id="2866c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2866c-132">RELATED LINKS</span></span>

[<span data-ttu-id="2866c-133">추가-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2866c-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="2866c-134">제거-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2866c-134">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

