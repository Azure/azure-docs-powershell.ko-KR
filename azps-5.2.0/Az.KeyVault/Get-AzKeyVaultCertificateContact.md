---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323518"
---
# <span data-ttu-id="c2c5e-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c2c5e-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="c2c5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c5e-103">키 자격 증명 모음에 대한 인증서 알림에 등록된 연락처를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2c5e-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="c2c5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2c5e-104">SYNTAX</span></span>

### <span data-ttu-id="c2c5e-105">VaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c2c5e-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2c5e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2c5e-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2c5e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2c5e-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2c5e-108">설명</span><span class="sxs-lookup"><span data-stu-id="c2c5e-108">DESCRIPTION</span></span>
<span data-ttu-id="c2c5e-109">**Get-AzKeyVaultCertificateContact** cmdlet은 Azure Key Vault의 키 자격 증명 모음에 대한 인증서 알림에 등록된 연락처를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2c5e-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c2c5e-110">예제</span><span class="sxs-lookup"><span data-stu-id="c2c5e-110">EXAMPLES</span></span>

### <span data-ttu-id="c2c5e-111">예제 1: 모든 인증서 연락처를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2c5e-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="c2c5e-112">이 명령은 Contoso 키 자격 증명 모음의 인증서 개체에 대한 모든 연락처를 택한 다음, $Contacts 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c5e-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="c2c5e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2c5e-113">PARAMETERS</span></span>

### <span data-ttu-id="c2c5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c5e-114">-DefaultProfile</span></span>
<span data-ttu-id="c2c5e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c2c5e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2c5e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2c5e-116">-InputObject</span></span>
<span data-ttu-id="c2c5e-117">KeyVault 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c2c5e-117">KeyVault object.</span></span>

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

### <span data-ttu-id="c2c5e-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2c5e-118">-ResourceId</span></span>
<span data-ttu-id="c2c5e-119">KeyVault ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c2c5e-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="c2c5e-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c2c5e-120">-VaultName</span></span>
<span data-ttu-id="c2c5e-121">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c5e-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="c2c5e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c5e-122">CommonParameters</span></span>
<span data-ttu-id="c2c5e-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c5e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c5e-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c2c5e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c5e-125">입력</span><span class="sxs-lookup"><span data-stu-id="c2c5e-125">INPUTS</span></span>

### <span data-ttu-id="c2c5e-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c2c5e-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c2c5e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c2c5e-127">System.String</span></span>

## <span data-ttu-id="c2c5e-128">출력</span><span class="sxs-lookup"><span data-stu-id="c2c5e-128">OUTPUTS</span></span>

### <span data-ttu-id="c2c5e-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c2c5e-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="c2c5e-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2c5e-130">NOTES</span></span>

## <span data-ttu-id="c2c5e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2c5e-131">RELATED LINKS</span></span>

[<span data-ttu-id="c2c5e-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c2c5e-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="c2c5e-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c2c5e-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

