---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 9c7b82c8ec884cc16bc3c593d9f00f1789b98e52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689666"
---
# <span data-ttu-id="f846a-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="f846a-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="f846a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f846a-102">SYNOPSIS</span></span>
<span data-ttu-id="f846a-103">키 자격 증명 모음에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f846a-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="f846a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f846a-104">SYNTAX</span></span>

### <span data-ttu-id="f846a-105">VaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f846a-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f846a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f846a-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f846a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f846a-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f846a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f846a-108">DESCRIPTION</span></span>
<span data-ttu-id="f846a-109">**AzKeyVaultCertificateContact** Cmdlet은 Azure key vault의 키 보관소에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f846a-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="f846a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f846a-110">EXAMPLES</span></span>

### <span data-ttu-id="f846a-111">예제 1: 모든 인증서 연락처 가져오기</span><span class="sxs-lookup"><span data-stu-id="f846a-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="f846a-112">이 명령은 Contoso 키 자격 증명 모음의 인증서 개체에 대 한 모든 연락처를 가져온 다음 $Contacts 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f846a-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="f846a-113">변수</span><span class="sxs-lookup"><span data-stu-id="f846a-113">PARAMETERS</span></span>

### <span data-ttu-id="f846a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f846a-114">-DefaultProfile</span></span>
<span data-ttu-id="f846a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f846a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f846a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f846a-116">-InputObject</span></span>
<span data-ttu-id="f846a-117">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="f846a-117">KeyVault object.</span></span>

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

### <span data-ttu-id="f846a-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f846a-118">-ResourceId</span></span>
<span data-ttu-id="f846a-119">KeyVault Id.</span><span class="sxs-lookup"><span data-stu-id="f846a-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="f846a-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f846a-120">-VaultName</span></span>
<span data-ttu-id="f846a-121">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f846a-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="f846a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f846a-122">CommonParameters</span></span>
<span data-ttu-id="f846a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f846a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f846a-124">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f846a-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f846a-125">입력</span><span class="sxs-lookup"><span data-stu-id="f846a-125">INPUTS</span></span>

### <span data-ttu-id="f846a-126">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f846a-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f846a-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f846a-127">System.String</span></span>

## <span data-ttu-id="f846a-128">출력</span><span class="sxs-lookup"><span data-stu-id="f846a-128">OUTPUTS</span></span>

### <span data-ttu-id="f846a-129">Microsoft. KeyVault. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="f846a-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="f846a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f846a-130">NOTES</span></span>

## <span data-ttu-id="f846a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f846a-131">RELATED LINKS</span></span>

[<span data-ttu-id="f846a-132">추가-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="f846a-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="f846a-133">제거-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="f846a-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

