---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048221"
---
# <span data-ttu-id="2b6a6-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2b6a6-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="2b6a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b6a6-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6a6-103">키 자격 증명 모음에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b6a6-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="2b6a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b6a6-104">SYNTAX</span></span>

### <span data-ttu-id="2b6a6-105">VaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2b6a6-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b6a6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2b6a6-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b6a6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b6a6-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b6a6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2b6a6-108">DESCRIPTION</span></span>
<span data-ttu-id="2b6a6-109">**AzKeyVaultCertificateContact** Cmdlet은 Azure key vault의 키 보관소에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b6a6-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="2b6a6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2b6a6-110">EXAMPLES</span></span>

### <span data-ttu-id="2b6a6-111">예제 1: 모든 인증서 연락처 가져오기</span><span class="sxs-lookup"><span data-stu-id="2b6a6-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="2b6a6-112">이 명령은 Contoso 키 자격 증명 모음의 인증서 개체에 대 한 모든 연락처를 가져온 다음 $Contacts 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b6a6-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="2b6a6-113">변수</span><span class="sxs-lookup"><span data-stu-id="2b6a6-113">PARAMETERS</span></span>

### <span data-ttu-id="2b6a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6a6-114">-DefaultProfile</span></span>
<span data-ttu-id="2b6a6-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2b6a6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6a6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b6a6-116">-InputObject</span></span>
<span data-ttu-id="2b6a6-117">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="2b6a6-117">KeyVault object.</span></span>

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

### <span data-ttu-id="2b6a6-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b6a6-118">-ResourceId</span></span>
<span data-ttu-id="2b6a6-119">KeyVault Id.</span><span class="sxs-lookup"><span data-stu-id="2b6a6-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="2b6a6-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2b6a6-120">-VaultName</span></span>
<span data-ttu-id="2b6a6-121">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b6a6-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="2b6a6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6a6-122">CommonParameters</span></span>
<span data-ttu-id="2b6a6-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b6a6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6a6-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b6a6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6a6-125">입력</span><span class="sxs-lookup"><span data-stu-id="2b6a6-125">INPUTS</span></span>

### <span data-ttu-id="2b6a6-126">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="2b6a6-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="2b6a6-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b6a6-127">System.String</span></span>

## <span data-ttu-id="2b6a6-128">출력</span><span class="sxs-lookup"><span data-stu-id="2b6a6-128">OUTPUTS</span></span>

### <span data-ttu-id="2b6a6-129">Microsoft. KeyVault. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2b6a6-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="2b6a6-130">상속자</span><span class="sxs-lookup"><span data-stu-id="2b6a6-130">NOTES</span></span>

## <span data-ttu-id="2b6a6-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b6a6-131">RELATED LINKS</span></span>

[<span data-ttu-id="2b6a6-132">추가-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2b6a6-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="2b6a6-133">제거-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2b6a6-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

