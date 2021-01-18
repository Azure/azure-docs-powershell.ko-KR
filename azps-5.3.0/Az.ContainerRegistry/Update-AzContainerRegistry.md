---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495842"
---
# <span data-ttu-id="eec71-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eec71-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="eec71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eec71-102">SYNOPSIS</span></span>
<span data-ttu-id="eec71-103">컨테이너 레지스트리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-103">Updates a container registry.</span></span>

## <span data-ttu-id="eec71-104">구문</span><span class="sxs-lookup"><span data-stu-id="eec71-104">SYNTAX</span></span>

### <span data-ttu-id="eec71-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="eec71-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec71-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eec71-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec71-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eec71-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec71-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eec71-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec71-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eec71-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec71-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eec71-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eec71-111">설명</span><span class="sxs-lookup"><span data-stu-id="eec71-111">DESCRIPTION</span></span>
<span data-ttu-id="eec71-112">Update-AzContainerRegistry cmdlet은 컨테이너 레지스트리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="eec71-113">예제</span><span class="sxs-lookup"><span data-stu-id="eec71-113">EXAMPLES</span></span>

### <span data-ttu-id="eec71-114">예제 1: 지정된 컨테이너 레지스트리에 대한 관리 사용자 사용</span><span class="sxs-lookup"><span data-stu-id="eec71-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="eec71-115">이 명령을 사용하면 지정된 컨테이너 레지스트리에 대한 관리 사용자가 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="eec71-116">예제 2: 지정된 컨테이너 레지스트리에서 사용하는 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="eec71-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="eec71-117">이 명령은 지정된 컨테이너 레지스트리를 설정하여 동일한 구독에서 기존 저장소 계정 \` mystorageaccount를 \` 사용하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="eec71-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eec71-118">PARAMETERS</span></span>

### <span data-ttu-id="eec71-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec71-119">-DefaultProfile</span></span>
<span data-ttu-id="eec71-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eec71-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eec71-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="eec71-121">-DisableAdminUser</span></span>
<span data-ttu-id="eec71-122">컨테이너 레지스트리에 대한 관리자 사용자를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec71-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="eec71-123">-EnableAdminUser</span></span>
<span data-ttu-id="eec71-124">컨테이너 레지스트리에 대한 관리자 사용자를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec71-125">-Name</span><span class="sxs-lookup"><span data-stu-id="eec71-125">-Name</span></span>
<span data-ttu-id="eec71-126">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec71-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="eec71-127">-NetworkRuleSet</span></span>
<span data-ttu-id="eec71-128">컨테이너 레지스트리에 대해 설정된 네트워크 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec71-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec71-129">-ResourceGroupName</span></span>
<span data-ttu-id="eec71-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec71-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eec71-131">-ResourceId</span></span>
<span data-ttu-id="eec71-132">컨테이너 레지스트리 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="eec71-132">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec71-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="eec71-133">-Sku</span></span>
<span data-ttu-id="eec71-134">Container Registry SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-134">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec71-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="eec71-135">-StorageAccountName</span></span>
<span data-ttu-id="eec71-136">기존 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-136">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec71-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="eec71-137">-Tag</span></span>
<span data-ttu-id="eec71-138">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="eec71-139">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="eec71-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec71-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eec71-140">-Confirm</span></span>
<span data-ttu-id="eec71-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec71-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec71-142">-WhatIf</span></span>
<span data-ttu-id="eec71-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="eec71-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eec71-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec71-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec71-145">CommonParameters</span></span>
<span data-ttu-id="eec71-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eec71-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec71-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eec71-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec71-148">입력</span><span class="sxs-lookup"><span data-stu-id="eec71-148">INPUTS</span></span>

### <span data-ttu-id="eec71-149">System.String</span><span class="sxs-lookup"><span data-stu-id="eec71-149">System.String</span></span>

## <span data-ttu-id="eec71-150">출력</span><span class="sxs-lookup"><span data-stu-id="eec71-150">OUTPUTS</span></span>

### <span data-ttu-id="eec71-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eec71-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="eec71-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eec71-152">NOTES</span></span>

## <span data-ttu-id="eec71-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eec71-153">RELATED LINKS</span></span>

[<span data-ttu-id="eec71-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eec71-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="eec71-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eec71-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="eec71-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eec71-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

