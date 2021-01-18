---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8a4c55f8b823a72224dc658a3ddc37ee867d781b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492869"
---
# <span data-ttu-id="17e28-101">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="17e28-101">Update-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="17e28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17e28-102">SYNOPSIS</span></span>
<span data-ttu-id="17e28-103">Azure 관리 HSM의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="17e28-104">구문</span><span class="sxs-lookup"><span data-stu-id="17e28-104">SYNTAX</span></span>

### <span data-ttu-id="17e28-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="17e28-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVaultManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e28-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17e28-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e28-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17e28-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17e28-108">설명</span><span class="sxs-lookup"><span data-stu-id="17e28-108">DESCRIPTION</span></span>
<span data-ttu-id="17e28-109">이 cmdlet은 Azure 관리 HSM의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="17e28-110">예제</span><span class="sxs-lookup"><span data-stu-id="17e28-110">EXAMPLES</span></span>

### <span data-ttu-id="17e28-111">예제 1: 직접 관리되는 Hsm 업데이트</span><span class="sxs-lookup"><span data-stu-id="17e28-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

Managed HSM Name                    : testmhsm
Resource Group Name                 : testmhsm
Location                            : eastus2euap
Resource ID                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testmhsm/provid
                                      ers/Microsoft.KeyVault/managedHSMs/testmhsm
HSM Pool URI                        :
Tenant ID                           : xxxxxx-xxxx-xxxx-xxxxxxxxxxxx
Initial Admin Object Ids            : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SKU                                 : StandardB1
Soft Delete Enabled?                : True
Enabled Purge Protection?           : False
Soft Delete Retention Period (days) : 90
Provisioning State                  : Provisioning
Status Message                      : Resource creation in progress. Starting service...
Tags                                :
                                      Name        Value
                                      ====        =====
                                      testKey     testValued
```

<span data-ttu-id="17e28-112">리소스 그룹에 명명된 관리되는 Hsm에 `$hsmName` 대한 태그를 업데이트합니다. `$resourceGroupName`</span><span class="sxs-lookup"><span data-stu-id="17e28-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="17e28-113">예제 2: 파이핑을 사용하여 관리되는 Hsm 업데이트</span><span class="sxs-lookup"><span data-stu-id="17e28-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzKeyVaultManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="17e28-114">파이핑 구문을 사용하여 관리되는 Hsm에 대한 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="17e28-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17e28-115">PARAMETERS</span></span>

### <span data-ttu-id="17e28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e28-116">-DefaultProfile</span></span>
<span data-ttu-id="17e28-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17e28-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17e28-118">-InputObject</span></span>
<span data-ttu-id="17e28-119">관리되는 HSM 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-119">Managed HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17e28-120">-Name</span><span class="sxs-lookup"><span data-stu-id="17e28-120">-Name</span></span>
<span data-ttu-id="17e28-121">관리되는 HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-121">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e28-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17e28-122">-ResourceGroupName</span></span>
<span data-ttu-id="17e28-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-123">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e28-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17e28-124">-ResourceId</span></span>
<span data-ttu-id="17e28-125">관리되는 HSM의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-125">Resource ID of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e28-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="17e28-126">-Tag</span></span>
<span data-ttu-id="17e28-127">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-127">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e28-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17e28-128">-Confirm</span></span>
<span data-ttu-id="17e28-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17e28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e28-130">-WhatIf</span></span>
<span data-ttu-id="17e28-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="17e28-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17e28-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17e28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e28-133">CommonParameters</span></span>
<span data-ttu-id="17e28-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17e28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e28-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="17e28-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e28-136">입력</span><span class="sxs-lookup"><span data-stu-id="17e28-136">INPUTS</span></span>

### <span data-ttu-id="17e28-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="17e28-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="17e28-138">System.String</span><span class="sxs-lookup"><span data-stu-id="17e28-138">System.String</span></span>

### <span data-ttu-id="17e28-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="17e28-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="17e28-140">출력</span><span class="sxs-lookup"><span data-stu-id="17e28-140">OUTPUTS</span></span>

### <span data-ttu-id="17e28-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="17e28-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="17e28-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17e28-142">NOTES</span></span>

## <span data-ttu-id="17e28-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17e28-143">RELATED LINKS</span></span>

[<span data-ttu-id="17e28-144">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="17e28-144">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="17e28-145">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="17e28-145">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="17e28-146">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="17e28-146">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)