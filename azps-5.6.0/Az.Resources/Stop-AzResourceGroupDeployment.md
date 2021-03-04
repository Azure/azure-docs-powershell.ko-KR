---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 9258c15578aaeae5102a5d60b2f18a8a4f179d76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967627"
---
# <span data-ttu-id="9f7ad-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9f7ad-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="9f7ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9f7ad-103">리소스 그룹 배포를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="9f7ad-104">구문</span><span class="sxs-lookup"><span data-stu-id="9f7ad-104">SYNTAX</span></span>

### <span data-ttu-id="9f7ad-105">StopByResourceGroupDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="9f7ad-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f7ad-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="9f7ad-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f7ad-107">설명</span><span class="sxs-lookup"><span data-stu-id="9f7ad-107">DESCRIPTION</span></span>
<span data-ttu-id="9f7ad-108">**Stop-AzResourceGroupDeployment** cmdlet은 시작했지만 완료되지 않은 Azure 리소스 그룹 배포를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="9f7ad-109">배포를 중지하려면 배포에 프로비전 또는 실패와 같은 완료된 상태가 아닌 프로비전과 같은 불완전한 프로비전 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="9f7ad-110">Azure 리소스는 웹 사이트, 데이터베이스 또는 데이터베이스 서버와 같은 사용자 관리 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="9f7ad-111">리소스 그룹은 단위로 배포되는 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="9f7ad-112">리소스 그룹을 배포하기 위해 New-AzResourceGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="9f7ad-113">New-AzResource cmdlet은 새 리소스를 생성하지만 이 cmdlet이 중지할 수 있는 리소스 그룹 배포 작업을 트리거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="9f7ad-114">이 cmdlet은 실행 중인 배포 하나만 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="9f7ad-115">이름 매개 *변수를* 사용하여 특정 배포를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="9f7ad-116">이름 매개 변수를 생략하면 **Stop-AzResourceGroupDeployment에서** 실행 중인 배포를 검색하고 중지합니다. </span><span class="sxs-lookup"><span data-stu-id="9f7ad-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="9f7ad-117">cmdlet에서 실행 중인 배포를 두 개 이상 찾은 경우 명령이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="9f7ad-118">예제</span><span class="sxs-lookup"><span data-stu-id="9f7ad-118">EXAMPLES</span></span>

### <span data-ttu-id="9f7ad-119">예제 1: 리소스 그룹 배포 시작 및 중지</span><span class="sxs-lookup"><span data-stu-id="9f7ad-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="9f7ad-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9f7ad-120">PARAMETERS</span></span>

### <span data-ttu-id="9f7ad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f7ad-121">-DefaultProfile</span></span>
<span data-ttu-id="9f7ad-122">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9f7ad-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f7ad-123">-Id</span><span class="sxs-lookup"><span data-stu-id="9f7ad-123">-Id</span></span>
<span data-ttu-id="9f7ad-124">중지할 리소스 그룹 배포의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-124">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f7ad-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9f7ad-125">-Name</span></span>
<span data-ttu-id="9f7ad-126">중지할 리소스 그룹 배포의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="9f7ad-127">이 매개 변수를 지정하지 않으면 이 cmdlet은 리소스 그룹에서 실행 중인 배포를 검색하고 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="9f7ad-128">실행 중인 배포가 두 개 이상 발견된 경우 명령이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="9f7ad-129">배포 이름을 얻으면 Get-AzResourceGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7ad-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="9f7ad-130">-Pre</span></span>
<span data-ttu-id="9f7ad-131">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9f7ad-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f7ad-132">-ResourceGroupName</span></span>
<span data-ttu-id="9f7ad-133">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="9f7ad-134">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹의 배포를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7ad-135">-확인</span><span class="sxs-lookup"><span data-stu-id="9f7ad-135">-Confirm</span></span>
<span data-ttu-id="9f7ad-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f7ad-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f7ad-137">-WhatIf</span></span>
<span data-ttu-id="9f7ad-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f7ad-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f7ad-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f7ad-140">CommonParameters</span></span>
<span data-ttu-id="9f7ad-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f7ad-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f7ad-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f7ad-143">입력</span><span class="sxs-lookup"><span data-stu-id="9f7ad-143">INPUTS</span></span>

### <span data-ttu-id="9f7ad-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9f7ad-144">System.String</span></span>

## <span data-ttu-id="9f7ad-145">출력</span><span class="sxs-lookup"><span data-stu-id="9f7ad-145">OUTPUTS</span></span>

### <span data-ttu-id="9f7ad-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f7ad-146">System.Boolean</span></span>

## <span data-ttu-id="9f7ad-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f7ad-147">NOTES</span></span>

## <span data-ttu-id="9f7ad-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f7ad-148">RELATED LINKS</span></span>

[<span data-ttu-id="9f7ad-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9f7ad-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="9f7ad-150">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="9f7ad-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="9f7ad-151">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f7ad-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="9f7ad-152">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9f7ad-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="9f7ad-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9f7ad-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="9f7ad-154">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9f7ad-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


