---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 9da5ee691b440ee24933d658dec3c85b1a7c8ced
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880625"
---
# <span data-ttu-id="d8f69-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8f69-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="d8f69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f69-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f69-103">리소스 그룹의 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8f69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8f69-104">SYNTAX</span></span>

### <span data-ttu-id="d8f69-105">GetByResourceGroupDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d8f69-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8f69-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d8f69-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8f69-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d8f69-107">DESCRIPTION</span></span>
<span data-ttu-id="d8f69-108">**AzureRmResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹의 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-108">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="d8f69-109">*이름* 또는 *Id* 매개 변수를 지정 하 여 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="d8f69-110">기본적으로 **Get-AzureRmResourceGroupDeployment** 는 지정 된 리소스 그룹에 대 한 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-110">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="d8f69-111">Azure 리소스는 사용자가 관리 하는 Azure 엔터티 (예: 데이터베이스 서버, 데이터베이스 또는 웹 사이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="d8f69-112">Azure 리소스 그룹은 하나의 단위로 배포 되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="d8f69-113">배포는 리소스 그룹의 리소스를 사용할 수 있도록 만드는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="d8f69-114">Azure 리소스 및 Azure 리소스 그룹에 대 한 자세한 내용은 New-AzureRmResourceGroup cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8f69-114">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="d8f69-115">추적에이 cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="d8f69-116">디버깅을 위해 Get-AzureRmLog cmdlet에이 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-116">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="d8f69-117">예제의</span><span class="sxs-lookup"><span data-stu-id="d8f69-117">EXAMPLES</span></span>

### <span data-ttu-id="d8f69-118">예제 1: 리소스 그룹에 대 한 모든 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="d8f69-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="d8f69-119">이 명령은 ContosoLabsRG 리소스 그룹에 대 한 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="d8f69-120">출력에는 갤러리 서식 파일을 사용 하는 WordPress 블로그의 배포가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="d8f69-121">예제 2: 이름으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="d8f69-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="d8f69-122">이 명령은 ContosoLabsRG 리소스 그룹의 DeployWebsite01 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="d8f69-123">**새 AzureRmResourceGroup** 또는 **AzureRmResourceGroupDeployment** cmdlet을 사용 하 여 배포에 이름을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-123">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="d8f69-124">이름을 할당 하지 않으면 cmdlet은 배포를 만드는 데 사용 되는 템플릿을 기반으로 하는 기본 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="d8f69-125">예제 3: 모든 리소스 그룹 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="d8f69-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="d8f69-126">이 명령은 Get-AzureRmResourceGroup cmdlet을 사용 하 여 구독에 있는 모든 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-126">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="d8f69-127">이 명령은 파이프라인 연산자를 사용 하 여 리소스 그룹을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d8f69-128">현재 cmdlet은 구독에 있는 모든 리소스 그룹의 모든 배포를 가져오고, 결과를 Format-Table cmdlet에 전달 하 여 **ResourceGroupName** , **Deploymentname** 및 **ProvisioningState** 속성 값을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="d8f69-129">변수</span><span class="sxs-lookup"><span data-stu-id="d8f69-129">PARAMETERS</span></span>

### <span data-ttu-id="d8f69-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d8f69-130">-ApiVersion</span></span>
<span data-ttu-id="d8f69-131">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d8f69-132">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d8f69-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f69-133">-DefaultProfile</span></span>
<span data-ttu-id="d8f69-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d8f69-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f69-135">-Id</span><span class="sxs-lookup"><span data-stu-id="d8f69-135">-Id</span></span>
<span data-ttu-id="d8f69-136">가져올 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="d8f69-137">-이름</span><span class="sxs-lookup"><span data-stu-id="d8f69-137">-Name</span></span>
<span data-ttu-id="d8f69-138">가져올 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="d8f69-139">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="d8f69-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="d8f69-140">-Pre</span></span>
<span data-ttu-id="d8f69-141">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d8f69-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f69-142">-ResourceGroupName</span></span>
<span data-ttu-id="d8f69-143">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d8f69-144">Cmdlet은이 매개 변수에서 지정 하는 리소스 그룹에 대 한 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="d8f69-145">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="d8f69-146">이 매개 변수는 필수 이며 각 명령에 하나의 리소스 그룹만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="d8f69-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f69-147">CommonParameters</span></span>
<span data-ttu-id="d8f69-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8f69-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f69-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8f69-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f69-150">입력</span><span class="sxs-lookup"><span data-stu-id="d8f69-150">INPUTS</span></span>

### <span data-ttu-id="d8f69-151">않아야</span><span class="sxs-lookup"><span data-stu-id="d8f69-151">None</span></span>

## <span data-ttu-id="d8f69-152">출력</span><span class="sxs-lookup"><span data-stu-id="d8f69-152">OUTPUTS</span></span>

### <span data-ttu-id="d8f69-153">ResourceManagement를 통해.</span><span class="sxs-lookup"><span data-stu-id="d8f69-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="d8f69-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8f69-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="d8f69-155">상속자</span><span class="sxs-lookup"><span data-stu-id="d8f69-155">NOTES</span></span>

## <span data-ttu-id="d8f69-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8f69-156">RELATED LINKS</span></span>

[<span data-ttu-id="d8f69-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8f69-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="d8f69-158">새로운 AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8f69-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="d8f69-159">새로운 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8f69-159">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d8f69-160">제거-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8f69-160">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d8f69-161">중지-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8f69-161">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d8f69-162">테스트-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8f69-162">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


