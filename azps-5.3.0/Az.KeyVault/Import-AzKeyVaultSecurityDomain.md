---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: f96aa323486144ec9d4dcb04ff00f408a763a81a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492885"
---
# <span data-ttu-id="ce4ae-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="ce4ae-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="ce4ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce4ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ce4ae-103">이전에 내보낼 보안 도메인 데이터를 관리되는 HSM으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="ce4ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce4ae-104">SYNTAX</span></span>

### <span data-ttu-id="ce4ae-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ce4ae-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce4ae-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ce4ae-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce4ae-107">설명</span><span class="sxs-lookup"><span data-stu-id="ce4ae-107">DESCRIPTION</span></span>
<span data-ttu-id="ce4ae-108">이 cmdlet은 이전에 내보낼 보안 도메인 데이터를 관리되는 HSM으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="ce4ae-109">예제</span><span class="sxs-lookup"><span data-stu-id="ce4ae-109">EXAMPLES</span></span>

### <span data-ttu-id="ce4ae-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ce4ae-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="ce4ae-111">먼저 보안 도메인 데이터의 암호를 해독하기 위해 키를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="ce4ae-112">그런 다음 **Import-AzKeyVaultSecurityDomain** 명령은 이러한 키를 사용하여 이전 백업된 보안 도메인 데이터를 관리되는 HSM으로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="ce4ae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce4ae-113">PARAMETERS</span></span>

### <span data-ttu-id="ce4ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce4ae-114">-DefaultProfile</span></span>
<span data-ttu-id="ce4ae-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce4ae-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce4ae-116">-InputObject</span></span>
<span data-ttu-id="ce4ae-117">관리되는 HSM을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-117">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ae-118">-Keys</span><span class="sxs-lookup"><span data-stu-id="ce4ae-118">-Keys</span></span>
<span data-ttu-id="ce4ae-119">보안 도메인 데이터의 암호를 해독하는 데 사용되는 키에 대한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="ce4ae-120">구성 방법에 대한 예제를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-120">See examples for how it is constructed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.SecurityDomain.Models.KeyPath[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ae-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ce4ae-121">-Name</span></span>
<span data-ttu-id="ce4ae-122">관리되는 HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ae-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce4ae-123">-PassThru</span></span>
<span data-ttu-id="ce4ae-124">지정하면 cmdlet이 성공하면 부울이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ae-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="ce4ae-125">-SecurityDomainPath</span></span>
<span data-ttu-id="ce4ae-126">암호화된 보안 도메인 데이터의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-126">Specify the path to the encrypted security domain data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ae-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce4ae-127">-Confirm</span></span>
<span data-ttu-id="ce4ae-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ae-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce4ae-129">-WhatIf</span></span>
<span data-ttu-id="ce4ae-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ce4ae-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce4ae-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce4ae-132">CommonParameters</span></span>
<span data-ttu-id="ce4ae-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce4ae-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ce4ae-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce4ae-135">입력</span><span class="sxs-lookup"><span data-stu-id="ce4ae-135">INPUTS</span></span>

### <span data-ttu-id="ce4ae-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ce4ae-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="ce4ae-137">출력</span><span class="sxs-lookup"><span data-stu-id="ce4ae-137">OUTPUTS</span></span>

### <span data-ttu-id="ce4ae-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ce4ae-138">System.Boolean</span></span>

## <span data-ttu-id="ce4ae-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce4ae-139">NOTES</span></span>

## <span data-ttu-id="ce4ae-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce4ae-140">RELATED LINKS</span></span>
