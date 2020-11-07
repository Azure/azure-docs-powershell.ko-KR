---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: dd61700c5f064a7bc1db84286252a57c18a212db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703232"
---
# <span data-ttu-id="26f9c-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26f9c-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="26f9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="26f9c-103">리소스 그룹의 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26f9c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26f9c-104">SYNTAX</span></span>

### <span data-ttu-id="26f9c-105">GetByResourceGroupDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="26f9c-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26f9c-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="26f9c-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26f9c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="26f9c-107">DESCRIPTION</span></span>
<span data-ttu-id="26f9c-108">**AzureRmResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹의 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-108">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="26f9c-109">*이름* 또는 *Id* 매개 변수를 지정 하 여 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="26f9c-110">기본적으로 **Get-AzureRmResourceGroupDeployment** 는 지정 된 리소스 그룹에 대 한 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-110">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>

<span data-ttu-id="26f9c-111">Azure 리소스는 사용자가 관리 하는 Azure 엔터티 (예: 데이터베이스 서버, 데이터베이스 또는 웹 사이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="26f9c-112">Azure 리소스 그룹은 하나의 단위로 배포 되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

<span data-ttu-id="26f9c-113">배포는 리소스 그룹의 리소스를 사용할 수 있도록 만드는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="26f9c-114">Azure 리소스 및 Azure 리소스 그룹에 대 한 자세한 내용은 New-AzureRmResourceGroup cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26f9c-114">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="26f9c-115">추적에이 cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="26f9c-116">디버깅을 위해 Get-AzureRmLog cmdlet에이 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-116">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="26f9c-117">예제의</span><span class="sxs-lookup"><span data-stu-id="26f9c-117">EXAMPLES</span></span>

### <span data-ttu-id="26f9c-118">예제 1: 리소스 그룹에 대 한 모든 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="26f9c-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="26f9c-119">이 명령은 ContosoLabsRG 리소스 그룹에 대 한 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="26f9c-120">출력에는 갤러리 서식 파일을 사용 하는 WordPress 블로그의 배포가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="26f9c-121">예제 2: 이름으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="26f9c-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="26f9c-122">이 명령은 ContosoLabsRG 리소스 그룹의 DeployWebsite01 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="26f9c-123">**새 AzureRmResourceGroup** 또는 **AzureRmResourceGroupDeployment** cmdlet을 사용 하 여 배포에 이름을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-123">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="26f9c-124">이름을 할당 하지 않으면 cmdlet은 배포를 만드는 데 사용 되는 템플릿을 기반으로 하는 기본 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="26f9c-125">예제 3: 모든 리소스 그룹 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="26f9c-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="26f9c-126">이 명령은 Get-AzureRmResourceGroup cmdlet을 사용 하 여 구독에 있는 모든 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-126">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="26f9c-127">이 명령은 파이프라인 연산자를 사용 하 여 리소스 그룹을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="26f9c-128">현재 cmdlet은 구독에 있는 모든 리소스 그룹의 모든 배포를 가져오고, 결과를 Format-Table cmdlet에 전달 하 여 **ResourceGroupName** , **Deploymentname** 및 **ProvisioningState** 속성 값을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="26f9c-129">변수</span><span class="sxs-lookup"><span data-stu-id="26f9c-129">PARAMETERS</span></span>

### <span data-ttu-id="26f9c-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="26f9c-130">-ApiVersion</span></span>
<span data-ttu-id="26f9c-131">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="26f9c-132">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="26f9c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f9c-133">-DefaultProfile</span></span>
<span data-ttu-id="26f9c-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="26f9c-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9c-135">-Id</span><span class="sxs-lookup"><span data-stu-id="26f9c-135">-Id</span></span>
<span data-ttu-id="26f9c-136">가져올 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-136">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9c-137">-이름</span><span class="sxs-lookup"><span data-stu-id="26f9c-137">-Name</span></span>
<span data-ttu-id="26f9c-138">가져올 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="26f9c-139">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-139">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f9c-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="26f9c-140">-Pre</span></span>
<span data-ttu-id="26f9c-141">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="26f9c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f9c-142">-ResourceGroupName</span></span>
<span data-ttu-id="26f9c-143">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="26f9c-144">Cmdlet은이 매개 변수에서 지정 하는 리소스 그룹에 대 한 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="26f9c-145">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="26f9c-146">이 매개 변수는 필수 이며 각 명령에 하나의 리소스 그룹만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-146">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f9c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f9c-147">CommonParameters</span></span>
<span data-ttu-id="26f9c-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f9c-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f9c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f9c-150">입력</span><span class="sxs-lookup"><span data-stu-id="26f9c-150">INPUTS</span></span>

### <span data-ttu-id="26f9c-151">않아야</span><span class="sxs-lookup"><span data-stu-id="26f9c-151">None</span></span>

## <span data-ttu-id="26f9c-152">출력</span><span class="sxs-lookup"><span data-stu-id="26f9c-152">OUTPUTS</span></span>

### <span data-ttu-id="26f9c-153">ResourceManagement. a m/. m a.</span><span class="sxs-lookup"><span data-stu-id="26f9c-153">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroupDeployment</span></span>
<span data-ttu-id="26f9c-154">Cmdlet은 리소스 그룹 배포를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f9c-154">The cmdlet returns resource group deployments.</span></span>

## <span data-ttu-id="26f9c-155">상속자</span><span class="sxs-lookup"><span data-stu-id="26f9c-155">NOTES</span></span>

## <span data-ttu-id="26f9c-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26f9c-156">RELATED LINKS</span></span>

[<span data-ttu-id="26f9c-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26f9c-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="26f9c-158">새로운 AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26f9c-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="26f9c-159">새로운 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26f9c-159">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="26f9c-160">제거-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26f9c-160">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="26f9c-161">중지-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26f9c-161">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="26f9c-162">테스트-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26f9c-162">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


