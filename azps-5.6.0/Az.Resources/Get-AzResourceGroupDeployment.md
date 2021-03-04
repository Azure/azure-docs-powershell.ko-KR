---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: eb79b6a46f2eaadfc6a42159706c37017cdac8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988932"
---
# <span data-ttu-id="741aa-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="741aa-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="741aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="741aa-102">SYNOPSIS</span></span>
<span data-ttu-id="741aa-103">리소스 그룹에서 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="741aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="741aa-104">SYNTAX</span></span>

### <span data-ttu-id="741aa-105">GetByResourceGroupDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="741aa-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="741aa-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="741aa-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="741aa-107">설명</span><span class="sxs-lookup"><span data-stu-id="741aa-107">DESCRIPTION</span></span>
<span data-ttu-id="741aa-108">**Get-AzResourceGroupDeployment** cmdlet은 Azure 리소스 그룹에 배포를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="741aa-109">결과를 필터링하기 위해 *이름* 또는 *ID 매개* 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="741aa-110">기본적으로 **Get-AzResourceGroupDeployment는** 지정된 리소스 그룹에 대한 모든 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="741aa-111">Azure 리소스는 데이터베이스 서버, 데이터베이스 또는 웹 사이트와 같은 사용자 관리 Azure 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="741aa-112">Azure 리소스 그룹은 단위로 배포되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="741aa-113">배포는 리소스 그룹의 리소스를 사용할 수 있도록 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="741aa-114">Azure 리소스 및 Azure 리소스 그룹에 대한 자세한 내용은 New-AzResourceGroup cmdlet을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="741aa-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="741aa-115">추적에 이 cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="741aa-116">디버깅의 경우 이 cmdlet을 Get-AzLog cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="741aa-117">예제</span><span class="sxs-lookup"><span data-stu-id="741aa-117">EXAMPLES</span></span>

### <span data-ttu-id="741aa-118">예제 1: 리소스 그룹에 대한 모든 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="741aa-119">이 명령은 ContosoLabsRG 리소스 그룹에 대한 모든 배포를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="741aa-120">출력은 갤러리 템플릿을 사용한 WordPress 블로그에 대한 배포를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="741aa-121">예제 2: 이름으로 배포하기</span><span class="sxs-lookup"><span data-stu-id="741aa-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="741aa-122">이 명령은 ContosoLabsRG 리소스 그룹의 DeployWebsite01 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="741aa-123">**New-AzResourceGroup** 또는 **New-AzResourceGroupDeployment** cmdlet을 사용하여 배포에 이름을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="741aa-124">이름을 할당하지 않는 경우 cmdlet은 배포를 만드는 데 사용되는 템플릿을 기반으로 기본 이름을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="741aa-125">예제 3: 모든 리소스 그룹의 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="741aa-126">이 명령은 Get-AzResourceGroup cmdlet을 사용하여 구독의 모든 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="741aa-127">명령은 파이프라인 연산자를 사용하여 리소스 그룹을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="741aa-128">현재 cmdlet은 구독의 모든 리소스 그룹의 모든 배포를 얻게 Format-Table cmdlet에 결과를 전달하여 **ResourceGroupName,** **DeploymentName** 및 **ProvisioningState** 속성 값을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="741aa-129">매개 변수</span><span class="sxs-lookup"><span data-stu-id="741aa-129">PARAMETERS</span></span>

### <span data-ttu-id="741aa-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741aa-130">-DefaultProfile</span></span>
<span data-ttu-id="741aa-131">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="741aa-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="741aa-132">-Id</span><span class="sxs-lookup"><span data-stu-id="741aa-132">-Id</span></span>
<span data-ttu-id="741aa-133">얻을 리소스 그룹 배포의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-133">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741aa-134">-Name</span><span class="sxs-lookup"><span data-stu-id="741aa-134">-Name</span></span>
<span data-ttu-id="741aa-135">얻을 배포의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="741aa-136">와일드카드 문자는 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-136">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="741aa-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="741aa-137">-Pre</span></span>
<span data-ttu-id="741aa-138">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="741aa-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="741aa-139">-ResourceGroupName</span></span>
<span data-ttu-id="741aa-140">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="741aa-141">cmdlet은 이 매개 변수가 지정하는 리소스 그룹에 대한 배포를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="741aa-142">와일드카드 문자는 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="741aa-143">이 매개 변수는 필수이기 때문에 각 명령에 하나의 리소스 그룹만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-143">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="741aa-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741aa-144">CommonParameters</span></span>
<span data-ttu-id="741aa-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="741aa-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741aa-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="741aa-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741aa-147">입력</span><span class="sxs-lookup"><span data-stu-id="741aa-147">INPUTS</span></span>

### <span data-ttu-id="741aa-148">System.String</span><span class="sxs-lookup"><span data-stu-id="741aa-148">System.String</span></span>

## <span data-ttu-id="741aa-149">출력</span><span class="sxs-lookup"><span data-stu-id="741aa-149">OUTPUTS</span></span>

### <span data-ttu-id="741aa-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="741aa-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="741aa-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="741aa-151">NOTES</span></span>

## <span data-ttu-id="741aa-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="741aa-152">RELATED LINKS</span></span>

[<span data-ttu-id="741aa-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="741aa-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="741aa-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="741aa-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="741aa-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="741aa-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="741aa-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="741aa-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="741aa-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="741aa-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="741aa-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="741aa-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


