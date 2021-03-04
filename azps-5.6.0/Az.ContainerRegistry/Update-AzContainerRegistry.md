---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: aa84186be2b5dc13117397e76722a6826d5314a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956315"
---
# <span data-ttu-id="1c843-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1c843-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="1c843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c843-102">SYNOPSIS</span></span>
<span data-ttu-id="1c843-103">컨테이너 레지스트리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-103">Updates a container registry.</span></span>

## <span data-ttu-id="1c843-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c843-104">SYNTAX</span></span>

### <span data-ttu-id="1c843-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c843-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c843-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c843-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c843-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c843-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c843-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c843-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c843-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c843-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c843-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c843-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c843-111">설명</span><span class="sxs-lookup"><span data-stu-id="1c843-111">DESCRIPTION</span></span>
<span data-ttu-id="1c843-112">Update-AzContainerRegistry cmdlet은 컨테이너 레지스트리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="1c843-113">예제</span><span class="sxs-lookup"><span data-stu-id="1c843-113">EXAMPLES</span></span>

### <span data-ttu-id="1c843-114">예제 1: 지정된 컨테이너 레지스트리에 대해 관리자 사용자 사용</span><span class="sxs-lookup"><span data-stu-id="1c843-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="1c843-115">이 명령을 사용하면 지정된 컨테이너 레지스트리에 대한 관리자 사용자를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="1c843-116">예제 2: 지정된 컨테이너 레지스트리에서 사용하는 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="1c843-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="1c843-117">이 명령은 지정된 컨테이너 레지스트리를 설정하여 동일한 구독에서 기존 저장소 계정 \` mystorageaccount를 \` 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="1c843-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1c843-118">PARAMETERS</span></span>

### <span data-ttu-id="1c843-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c843-119">-DefaultProfile</span></span>
<span data-ttu-id="1c843-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1c843-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c843-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="1c843-121">-DisableAdminUser</span></span>
<span data-ttu-id="1c843-122">컨테이너 레지스트리에 대한 관리자 사용자를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="1c843-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="1c843-123">-EnableAdminUser</span></span>
<span data-ttu-id="1c843-124">컨테이너 레지스트리에 대한 관리자 사용자를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="1c843-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1c843-125">-Name</span></span>
<span data-ttu-id="1c843-126">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="1c843-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1c843-127">-NetworkRuleSet</span></span>
<span data-ttu-id="1c843-128">컨테이너 레지스트리에 대한 네트워크 규칙 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-128">The network rule set for a container registry.</span></span>

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

### <span data-ttu-id="1c843-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c843-129">-ResourceGroupName</span></span>
<span data-ttu-id="1c843-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="1c843-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c843-131">-ResourceId</span></span>
<span data-ttu-id="1c843-132">컨테이너 레지스트리 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1c843-132">The container registry resource id</span></span>

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

### <span data-ttu-id="1c843-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="1c843-133">-Sku</span></span>
<span data-ttu-id="1c843-134">컨테이너 레지스트리 SKU.</span><span class="sxs-lookup"><span data-stu-id="1c843-134">Container Registry SKU.</span></span>

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

### <span data-ttu-id="1c843-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1c843-135">-StorageAccountName</span></span>
<span data-ttu-id="1c843-136">기존 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="1c843-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c843-137">-Tag</span></span>
<span data-ttu-id="1c843-138">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="1c843-139">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1c843-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1c843-140">-확인</span><span class="sxs-lookup"><span data-stu-id="1c843-140">-Confirm</span></span>
<span data-ttu-id="1c843-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c843-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c843-142">-WhatIf</span></span>
<span data-ttu-id="1c843-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c843-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c843-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c843-145">CommonParameters</span></span>
<span data-ttu-id="1c843-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c843-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c843-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c843-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c843-148">입력</span><span class="sxs-lookup"><span data-stu-id="1c843-148">INPUTS</span></span>

### <span data-ttu-id="1c843-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1c843-149">System.String</span></span>

## <span data-ttu-id="1c843-150">출력</span><span class="sxs-lookup"><span data-stu-id="1c843-150">OUTPUTS</span></span>

### <span data-ttu-id="1c843-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1c843-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="1c843-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c843-152">NOTES</span></span>

## <span data-ttu-id="1c843-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c843-153">RELATED LINKS</span></span>

[<span data-ttu-id="1c843-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1c843-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="1c843-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1c843-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="1c843-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1c843-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

