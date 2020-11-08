---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: f743b408917e575005589598a49fafbd8cc95379
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226913"
---
# <span data-ttu-id="310cf-101">Restore-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="310cf-101">Restore-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="310cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="310cf-102">SYNOPSIS</span></span>
<span data-ttu-id="310cf-103">관리 되는 HSM으로 이전에 백업한 보안 도메인 데이터를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-103">Restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="310cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="310cf-104">SYNTAX</span></span>

### <span data-ttu-id="310cf-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="310cf-105">ByName (Default)</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="310cf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="310cf-106">ByInputObject</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="310cf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="310cf-107">DESCRIPTION</span></span>
<span data-ttu-id="310cf-108">이 cmdlet은 이전에 백업한 보안 도메인 데이터를 관리 되는 HSM에 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-108">This cmdlet restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="310cf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="310cf-109">EXAMPLES</span></span>

### <span data-ttu-id="310cf-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="310cf-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Restore-AzManagedHsmSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="310cf-111">먼저 보안 도메인 데이터를 해독 하는 데 키를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-111">First, the keys need be provided to decrypt the security domain data.</span></span> <span data-ttu-id="310cf-112">그런 다음 **Restore-AzManagedHsmSecurityDomain** 명령은 이러한 키를 사용 하 여 이전에 백업한 보안 도메인 데이터를 관리 되는 HSM으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-112">Then, The **Restore-AzManagedHsmSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="310cf-113">변수</span><span class="sxs-lookup"><span data-stu-id="310cf-113">PARAMETERS</span></span>

### <span data-ttu-id="310cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310cf-114">-DefaultProfile</span></span>
<span data-ttu-id="310cf-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="310cf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="310cf-116">-InputObject</span></span>
<span data-ttu-id="310cf-117">관리 되는 HSM을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="310cf-118">-키</span><span class="sxs-lookup"><span data-stu-id="310cf-118">-Keys</span></span>
<span data-ttu-id="310cf-119">보안 도메인 데이터의 암호를 해독 하는 데 사용 되는 키에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="310cf-120">생성 방법에 대 한 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="310cf-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="310cf-121">-이름</span><span class="sxs-lookup"><span data-stu-id="310cf-121">-Name</span></span>
<span data-ttu-id="310cf-122">관리 되는 HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="310cf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="310cf-123">-PassThru</span></span>
<span data-ttu-id="310cf-124">지정 되 면 cmdlet이 성공할 때 부울이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="310cf-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="310cf-125">-SecurityDomainPath</span></span>
<span data-ttu-id="310cf-126">암호화 된 보안 도메인 데이터의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="310cf-127">-확인</span><span class="sxs-lookup"><span data-stu-id="310cf-127">-Confirm</span></span>
<span data-ttu-id="310cf-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="310cf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="310cf-129">-WhatIf</span></span>
<span data-ttu-id="310cf-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="310cf-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="310cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310cf-132">CommonParameters</span></span>
<span data-ttu-id="310cf-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="310cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310cf-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="310cf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310cf-135">입력</span><span class="sxs-lookup"><span data-stu-id="310cf-135">INPUTS</span></span>

### <span data-ttu-id="310cf-136">Microsoft. KeyVault. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="310cf-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="310cf-137">출력</span><span class="sxs-lookup"><span data-stu-id="310cf-137">OUTPUTS</span></span>

### <span data-ttu-id="310cf-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="310cf-138">System.Boolean</span></span>

## <span data-ttu-id="310cf-139">상속자</span><span class="sxs-lookup"><span data-stu-id="310cf-139">NOTES</span></span>

## <span data-ttu-id="310cf-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="310cf-140">RELATED LINKS</span></span>
