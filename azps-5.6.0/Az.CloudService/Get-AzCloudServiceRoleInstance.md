---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 516bc63d7866ffd8a3c16fd224a49697c0cc972f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001803"
---
# <span data-ttu-id="8786e-101">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="8786e-101">Get-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="8786e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8786e-102">SYNOPSIS</span></span>
<span data-ttu-id="8786e-103">클라우드 서비스에서 역할 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-103">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="8786e-104">구문</span><span class="sxs-lookup"><span data-stu-id="8786e-104">SYNTAX</span></span>

### <span data-ttu-id="8786e-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="8786e-105">List (Default)</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8786e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="8786e-106">Get</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8786e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8786e-107">GetViaIdentity</span></span>
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8786e-108">설명</span><span class="sxs-lookup"><span data-stu-id="8786e-108">DESCRIPTION</span></span>
<span data-ttu-id="8786e-109">클라우드 서비스에서 역할 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-109">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="8786e-110">예제</span><span class="sxs-lookup"><span data-stu-id="8786e-110">EXAMPLES</span></span>

### <span data-ttu-id="8786e-111">예제 1: 모든 역할 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-111">Example 1: Get all role instances</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="8786e-112">이 명령은 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 클라우드 서비스의 모든 역할 인스턴스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-112">This command gets the properties of all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="8786e-113">예제 2: 단일 역할 인스턴스에 대한 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="8786e-113">Example 2: Get properties for single role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="8786e-114">이 명령은 ContosOrg라는 리소스 그룹에 ContosoFrontEnd_IN_0 ContosoCS라는 클라우드 서비스의 역할 인스턴스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-114">This command gets the properties of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="8786e-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8786e-115">PARAMETERS</span></span>

### <span data-ttu-id="8786e-116">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="8786e-116">-CloudServiceName</span></span>
<span data-ttu-id="8786e-117">.</span><span class="sxs-lookup"><span data-stu-id="8786e-117">.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8786e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8786e-118">-DefaultProfile</span></span>
<span data-ttu-id="8786e-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8786e-120">-확장</span><span class="sxs-lookup"><span data-stu-id="8786e-120">-Expand</span></span>
<span data-ttu-id="8786e-121">작업에 적용할 확장 식입니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-121">The expand expression to apply to the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.InstanceViewTypes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8786e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8786e-122">-InputObject</span></span>
<span data-ttu-id="8786e-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8786e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8786e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8786e-124">-ResourceGroupName</span></span>
<span data-ttu-id="8786e-125">.</span><span class="sxs-lookup"><span data-stu-id="8786e-125">.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8786e-126">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="8786e-126">-RoleInstanceName</span></span>
<span data-ttu-id="8786e-127">역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-127">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8786e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8786e-128">-SubscriptionId</span></span>
<span data-ttu-id="8786e-129">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8786e-130">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8786e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8786e-131">CommonParameters</span></span>
<span data-ttu-id="8786e-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8786e-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8786e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8786e-134">입력</span><span class="sxs-lookup"><span data-stu-id="8786e-134">INPUTS</span></span>

### <span data-ttu-id="8786e-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="8786e-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="8786e-136">출력</span><span class="sxs-lookup"><span data-stu-id="8786e-136">OUTPUTS</span></span>

### <span data-ttu-id="8786e-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span><span class="sxs-lookup"><span data-stu-id="8786e-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span></span>

## <span data-ttu-id="8786e-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8786e-138">NOTES</span></span>

<span data-ttu-id="8786e-139">별칭</span><span class="sxs-lookup"><span data-stu-id="8786e-139">ALIASES</span></span>

<span data-ttu-id="8786e-140">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8786e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8786e-141">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8786e-142">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8786e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8786e-143">INPUTOBJECT <ICloudServiceIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8786e-143">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8786e-144">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="8786e-144">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="8786e-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="8786e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8786e-146">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="8786e-146">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="8786e-147">`[RoleInstanceName <String>]`: 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-147">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="8786e-148">`[RoleName <String>]`: 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-148">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="8786e-149">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8786e-150">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-150">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8786e-151">`[UpdateDomain <Int32?>]`: 업데이트 도메인을 식별하는 정수 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-151">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="8786e-152">업데이트 도메인은 0 기반 인덱스로 식별됩니다. 첫 번째 업데이트 도메인에는 ID가 0이고, 두 번째 도메인에는 1의 ID가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8786e-152">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="8786e-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8786e-153">RELATED LINKS</span></span>

