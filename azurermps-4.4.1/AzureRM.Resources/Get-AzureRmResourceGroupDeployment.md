---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532988"
---
# <span data-ttu-id="0845f-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0845f-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="0845f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0845f-102">SYNOPSIS</span></span>
<span data-ttu-id="0845f-103">리소스 그룹의 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0845f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0845f-104">SYNTAX</span></span>

### <span data-ttu-id="0845f-105">배포 이름 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="0845f-105">The deployment name parameter set.</span></span> <span data-ttu-id="0845f-106">기본값</span><span class="sxs-lookup"><span data-stu-id="0845f-106">(Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0845f-107">배포 Id 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="0845f-107">The deployment Id parameter set.</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0845f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0845f-108">DESCRIPTION</span></span>
<span data-ttu-id="0845f-109">**AzureRmResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹의 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-109">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="0845f-110">*이름* 또는 *Id* 매개 변수를 지정 하 여 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-110">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="0845f-111">기본적으로 **Get-AzureRmResourceGroupDeployment** 는 지정 된 리소스 그룹에 대 한 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-111">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>

<span data-ttu-id="0845f-112">Azure 리소스는 사용자가 관리 하는 Azure 엔터티 (예: 데이터베이스 서버, 데이터베이스 또는 웹 사이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-112">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="0845f-113">Azure 리소스 그룹은 하나의 단위로 배포 되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-113">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

<span data-ttu-id="0845f-114">배포는 리소스 그룹의 리소스를 사용할 수 있도록 만드는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-114">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="0845f-115">Azure 리소스 및 Azure 리소스 그룹에 대 한 자세한 내용은 New-AzureRmResourceGroup cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0845f-115">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="0845f-116">추적에이 cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-116">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="0845f-117">디버깅을 위해 Get-AzureRmLog cmdlet에이 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-117">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="0845f-118">예제의</span><span class="sxs-lookup"><span data-stu-id="0845f-118">EXAMPLES</span></span>

### <span data-ttu-id="0845f-119">예제 1: 리소스 그룹에 대 한 모든 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="0845f-119">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="0845f-120">이 명령은 ContosoLabsRG 리소스 그룹에 대 한 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-120">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="0845f-121">출력에는 갤러리 서식 파일을 사용 하는 WordPress 블로그의 배포가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-121">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="0845f-122">예제 2: 이름으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="0845f-122">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="0845f-123">이 명령은 ContosoLabsRG 리소스 그룹의 DeployWebsite01 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-123">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="0845f-124">**새 AzureRmResourceGroup** 또는 **AzureRmResourceGroupDeployment** cmdlet을 사용 하 여 배포에 이름을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-124">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="0845f-125">이름을 할당 하지 않으면 cmdlet은 배포를 만드는 데 사용 되는 템플릿을 기반으로 하는 기본 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-125">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="0845f-126">예제 3: 모든 리소스 그룹 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="0845f-126">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="0845f-127">이 명령은 Get-AzureRmResourceGroup cmdlet을 사용 하 여 구독에 있는 모든 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-127">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="0845f-128">이 명령은 파이프라인 연산자를 사용 하 여 리소스 그룹을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-128">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0845f-129">현재 cmdlet은 구독에 있는 모든 리소스 그룹의 모든 배포를 가져오고, 결과를 Format-Table cmdlet에 전달 하 여 **ResourceGroupName** , **Deploymentname** 및 **ProvisioningState** 속성 값을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-129">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="0845f-130">변수</span><span class="sxs-lookup"><span data-stu-id="0845f-130">PARAMETERS</span></span>

### <span data-ttu-id="0845f-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0845f-131">-ApiVersion</span></span>
<span data-ttu-id="0845f-132">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-132">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0845f-133">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-133">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0845f-134">-Id</span><span class="sxs-lookup"><span data-stu-id="0845f-134">-Id</span></span>
<span data-ttu-id="0845f-135">가져올 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-135">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0845f-136">-이름</span><span class="sxs-lookup"><span data-stu-id="0845f-136">-Name</span></span>
<span data-ttu-id="0845f-137">가져올 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-137">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="0845f-138">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0845f-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="0845f-139">-Pre</span></span>
<span data-ttu-id="0845f-140">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0845f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0845f-141">-ResourceGroupName</span></span>
<span data-ttu-id="0845f-142">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0845f-143">Cmdlet은이 매개 변수에서 지정 하는 리소스 그룹에 대 한 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-143">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="0845f-144">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-144">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="0845f-145">이 매개 변수는 필수 이며 각 명령에 하나의 리소스 그룹만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-145">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0845f-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0845f-146">-DefaultProfile</span></span>
<span data-ttu-id="0845f-147">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0845f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0845f-148">CommonParameters</span></span>
<span data-ttu-id="0845f-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0845f-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0845f-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0845f-151">입력</span><span class="sxs-lookup"><span data-stu-id="0845f-151">INPUTS</span></span>

### <span data-ttu-id="0845f-152">않아야</span><span class="sxs-lookup"><span data-stu-id="0845f-152">None</span></span>

## <span data-ttu-id="0845f-153">출력</span><span class="sxs-lookup"><span data-stu-id="0845f-153">OUTPUTS</span></span>

### <span data-ttu-id="0845f-154">ResourceManagement. a m/. m a.</span><span class="sxs-lookup"><span data-stu-id="0845f-154">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroupDeployment</span></span>
<span data-ttu-id="0845f-155">Cmdlet은 리소스 그룹 배포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0845f-155">The cmdlet returns resource group deployments.</span></span>

## <span data-ttu-id="0845f-156">상속자</span><span class="sxs-lookup"><span data-stu-id="0845f-156">NOTES</span></span>

## <span data-ttu-id="0845f-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0845f-157">RELATED LINKS</span></span>

[<span data-ttu-id="0845f-158">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0845f-158">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="0845f-159">새로운 AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0845f-159">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="0845f-160">새로운 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0845f-160">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="0845f-161">제거-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0845f-161">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="0845f-162">중지-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0845f-162">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="0845f-163">테스트-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0845f-163">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


