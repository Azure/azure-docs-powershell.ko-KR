---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348633"
---
# <span data-ttu-id="3544c-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="3544c-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="3544c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3544c-102">SYNOPSIS</span></span>
<span data-ttu-id="3544c-103">노드 형식에 vm 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="3544c-104">구문</span><span class="sxs-lookup"><span data-stu-id="3544c-104">SYNTAX</span></span>

### <span data-ttu-id="3544c-105">ByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="3544c-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3544c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3544c-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3544c-107">설명</span><span class="sxs-lookup"><span data-stu-id="3544c-107">DESCRIPTION</span></span>
<span data-ttu-id="3544c-108">노드 유형에 vm 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-108">Add vm extension to the node type.</span></span> <span data-ttu-id="3544c-109">그러면 확장이 밑이 있는 Virtual Machine Scale Set 리소스에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="3544c-110">예제</span><span class="sxs-lookup"><span data-stu-id="3544c-110">EXAMPLES</span></span>

### <span data-ttu-id="3544c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3544c-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="3544c-112">이 명령은 노드 형식에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="3544c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3544c-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="3544c-114">이 명령은 설정 및 보호된 설정이 있는 확장을 노드 유형에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="3544c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="3544c-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="3544c-116">이 명령은 파이핑을 사용하여 노드 형식에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="3544c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3544c-117">PARAMETERS</span></span>

### <span data-ttu-id="3544c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3544c-118">-AsJob</span></span>
<span data-ttu-id="3544c-119">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3544c-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3544c-121">배포 시 사용할 수 있는 경우 확장에서 최신 부 버전을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="3544c-122">그러나 배포된 후 이 속성을 true로 설정한 경우에도 재배포하지 않는 한 확장은 부 버전을 업그레이드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3544c-123">-ClusterName</span></span>
<span data-ttu-id="3544c-124">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-124">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3544c-125">-DefaultProfile</span></span>
<span data-ttu-id="3544c-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="3544c-127">-ForceUpdateTag</span></span>
<span data-ttu-id="3544c-128">값이 제공되고 이전 값과 다른 경우 확장 구성이 변경되지 않은 경우에도 확장 처리기에서 강제로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3544c-129">-InputObject</span></span>
<span data-ttu-id="3544c-130">노드 유형 리소스</span><span class="sxs-lookup"><span data-stu-id="3544c-130">Node Type resource</span></span>

```yaml
Type: PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="3544c-131">-Name</span></span>
<span data-ttu-id="3544c-132">확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-132">extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="3544c-133">-NodeTypeName</span></span>
<span data-ttu-id="3544c-134">노드 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-134">Specify the name of the node type.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="3544c-135">-ProtectedSetting</span></span>
<span data-ttu-id="3544c-136">확장은 protectedSettings 또는 protectedSettingsFromKeyVault를 포함하거나 보호된 설정을 모두 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="3544c-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="3544c-138">이 확장을 프로비전해야 하는 확장 이름의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3544c-139">-Publisher</span></span>
<span data-ttu-id="3544c-140">확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="3544c-141">이 경우 Get-AzVMImagePublisher cmdlet을 사용하여 게시자를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3544c-142">-ResourceGroupName</span></span>
<span data-ttu-id="3544c-143">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-143">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-144">-Setting</span><span class="sxs-lookup"><span data-stu-id="3544c-144">-Setting</span></span>
<span data-ttu-id="3544c-145">확장에 대한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-146">-Type</span><span class="sxs-lookup"><span data-stu-id="3544c-146">-Type</span></span>
<span data-ttu-id="3544c-147">확장의 유형을 지정합니다. 예를 들어 "CustomScriptExtension"입니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="3544c-148">확장 형식을 Get-AzVMExtensionImageType cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3544c-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="3544c-150">스크립트 처리기 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-150">Specifies the version of the script handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3544c-151">-Confirm</span></span>
<span data-ttu-id="3544c-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3544c-153">-WhatIf</span></span>
<span data-ttu-id="3544c-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3544c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3544c-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3544c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3544c-156">CommonParameters</span></span>
<span data-ttu-id="3544c-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3544c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3544c-158">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3544c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3544c-159">입력</span><span class="sxs-lookup"><span data-stu-id="3544c-159">INPUTS</span></span>

### <span data-ttu-id="3544c-160">System.String</span><span class="sxs-lookup"><span data-stu-id="3544c-160">System.String</span></span>

### <span data-ttu-id="3544c-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3544c-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="3544c-162">출력</span><span class="sxs-lookup"><span data-stu-id="3544c-162">OUTPUTS</span></span>

### <span data-ttu-id="3544c-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3544c-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="3544c-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3544c-164">NOTES</span></span>

## <span data-ttu-id="3544c-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3544c-165">RELATED LINKS</span></span>
