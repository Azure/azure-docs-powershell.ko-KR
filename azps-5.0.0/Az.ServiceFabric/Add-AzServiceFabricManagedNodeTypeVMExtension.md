---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226517"
---
# <span data-ttu-id="c2d8e-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="c2d8e-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="c2d8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d8e-103">노드 형식에 vm 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="c2d8e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2d8e-104">SYNTAX</span></span>

### <span data-ttu-id="c2d8e-105">ByObj (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2d8e-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2d8e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c2d8e-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2d8e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c2d8e-107">DESCRIPTION</span></span>
<span data-ttu-id="c2d8e-108">노드 형식에 vm 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-108">Add vm extension to the node type.</span></span> <span data-ttu-id="c2d8e-109">이렇게 하면 확장은 가상 컴퓨터 확장 집합 리소스에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="c2d8e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c2d8e-110">EXAMPLES</span></span>

### <span data-ttu-id="c2d8e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2d8e-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="c2d8e-112">이 명령은 노드 형식에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="c2d8e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c2d8e-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="c2d8e-114">이 명령은 설정 및 보호 된 설정과 함께 확장을 노드 형식에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="c2d8e-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="c2d8e-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="c2d8e-116">이 명령은 노드 형식에 파이핑을 사용 하 여 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="c2d8e-117">변수</span><span class="sxs-lookup"><span data-stu-id="c2d8e-117">PARAMETERS</span></span>

### <span data-ttu-id="c2d8e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2d8e-118">-AsJob</span></span>
<span data-ttu-id="c2d8e-119">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c2d8e-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c2d8e-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c2d8e-121">배포 시 사용할 수 있는 확장이 새 부 버전을 사용 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="c2d8e-122">그러나 배포 된 후에는이 속성이 true로 설정 된 경우에도 확장에서 부 버전이 업그레이드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="c2d8e-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c2d8e-123">-ClusterName</span></span>
<span data-ttu-id="c2d8e-124">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c2d8e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d8e-125">-DefaultProfile</span></span>
<span data-ttu-id="c2d8e-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2d8e-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="c2d8e-127">-ForceUpdateTag</span></span>
<span data-ttu-id="c2d8e-128">값이 제공 되 고 이전 값과 다른 경우 확장 구성이 변경 되지 않았더라도 확장 처리기가 강제로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="c2d8e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2d8e-129">-InputObject</span></span>
<span data-ttu-id="c2d8e-130">노드 형식 리소스</span><span class="sxs-lookup"><span data-stu-id="c2d8e-130">Node Type resource</span></span>

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

### <span data-ttu-id="c2d8e-131">-이름</span><span class="sxs-lookup"><span data-stu-id="c2d8e-131">-Name</span></span>
<span data-ttu-id="c2d8e-132">확장명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-132">extension name.</span></span>

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

### <span data-ttu-id="c2d8e-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="c2d8e-133">-NodeTypeName</span></span>
<span data-ttu-id="c2d8e-134">노드 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-134">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="c2d8e-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="c2d8e-135">-ProtectedSetting</span></span>
<span data-ttu-id="c2d8e-136">확장명에는 protectedSettings 또는 protectedSettingsFromKeyVault를 포함할 수도 있고 보호 되는 설정이 전혀 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="c2d8e-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="c2d8e-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="c2d8e-138">이 확장을 프로 비전 해야 하는 확장명 이름 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="c2d8e-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c2d8e-139">-Publisher</span></span>
<span data-ttu-id="c2d8e-140">확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="c2d8e-141">이는 Get-AzVMImagePublisher cmdlet을 사용 하 여 게시자를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="c2d8e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2d8e-142">-ResourceGroupName</span></span>
<span data-ttu-id="c2d8e-143">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-143">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c2d8e-144">-설정</span><span class="sxs-lookup"><span data-stu-id="c2d8e-144">-Setting</span></span>
<span data-ttu-id="c2d8e-145">확장에 대 한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="c2d8e-146">-Type</span><span class="sxs-lookup"><span data-stu-id="c2d8e-146">-Type</span></span>
<span data-ttu-id="c2d8e-147">확장명의 유형을 지정 합니다. 예를 들어 "CustomScriptExtension"이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="c2d8e-148">Get-AzVMExtensionImageType cmdlet을 사용 하 여 확장 형식을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="c2d8e-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c2d8e-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="c2d8e-150">스크립트 처리기의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-150">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="c2d8e-151">-확인</span><span class="sxs-lookup"><span data-stu-id="c2d8e-151">-Confirm</span></span>
<span data-ttu-id="c2d8e-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2d8e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2d8e-153">-WhatIf</span></span>
<span data-ttu-id="c2d8e-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2d8e-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2d8e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d8e-156">CommonParameters</span></span>
<span data-ttu-id="c2d8e-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d8e-158">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d8e-159">입력</span><span class="sxs-lookup"><span data-stu-id="c2d8e-159">INPUTS</span></span>

### <span data-ttu-id="c2d8e-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c2d8e-160">System.String</span></span>

### <span data-ttu-id="c2d8e-161">ServiceFabric. a i m.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="c2d8e-162">출력</span><span class="sxs-lookup"><span data-stu-id="c2d8e-162">OUTPUTS</span></span>

### <span data-ttu-id="c2d8e-163">ServiceFabric. a i m.</span><span class="sxs-lookup"><span data-stu-id="c2d8e-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="c2d8e-164">상속자</span><span class="sxs-lookup"><span data-stu-id="c2d8e-164">NOTES</span></span>

## <span data-ttu-id="c2d8e-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2d8e-165">RELATED LINKS</span></span>
