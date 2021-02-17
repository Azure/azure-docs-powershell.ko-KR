---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
ms.openlocfilehash: faab9e645f05b8b661b03911bcba517e770f4d78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205088"
---
# <span data-ttu-id="4d121-101">Get-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="4d121-101">Get-AzCloudService</span></span>

## <span data-ttu-id="4d121-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d121-102">SYNOPSIS</span></span>
<span data-ttu-id="4d121-103">클라우드 서비스에 대한 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-103">Display information about a cloud service.</span></span>

## <span data-ttu-id="4d121-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d121-104">SYNTAX</span></span>

### <span data-ttu-id="4d121-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="4d121-105">List (Default)</span></span>
```
Get-AzCloudService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d121-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="4d121-106">Get</span></span>
```
Get-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d121-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d121-107">GetViaIdentity</span></span>
```
Get-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d121-108">List1</span><span class="sxs-lookup"><span data-stu-id="4d121-108">List1</span></span>
```
Get-AzCloudService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d121-109">설명</span><span class="sxs-lookup"><span data-stu-id="4d121-109">DESCRIPTION</span></span>
<span data-ttu-id="4d121-110">클라우드 서비스에 대한 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-110">Display information about a cloud service.</span></span>

## <span data-ttu-id="4d121-111">예제</span><span class="sxs-lookup"><span data-stu-id="4d121-111">EXAMPLES</span></span>

### <span data-ttu-id="4d121-112">예제 1: 리소스 그룹에서 모든 클라우드 서비스 얻기</span><span class="sxs-lookup"><span data-stu-id="4d121-112">Example 1: Get all cloud service under a resource group</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded
ContosOrg         ContosoCSTest     eastus2euap Failed
```

<span data-ttu-id="4d121-113">이 명령은 ContosOrg라는 리소스 그룹의 모든 클라우드 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-113">This command gets all cloud services in resource group named ContosOrg</span></span>

### <span data-ttu-id="4d121-114">예제 2: 클라우드 서비스 얻기</span><span class="sxs-lookup"><span data-stu-id="4d121-114">Example 2: Get cloud service</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded

PS C:\> $cloudService = Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
PS C:\> $cloudService | Format-List
ResourceGroupName : ContosOrg
Configuration     : xxxxxxxx
ConfigurationUrl  :
ExtensionProfile  : xxxxxxxx
Id                : xxxxxxxx
Location          : East US
Name              : ContosoCS
NetworkProfile    : xxxxxxxx
OSProfile         : xxxxxxxx
PackageUrl        : xxxxxxxx
ProvisioningState : Succeeded
RoleProfile       : xxxxxxxx
StartCloudService :
Tag               : {
                      "Owner": "Contos"
                    }
Type              : Microsoft.Compute/cloudServices
UniqueId          : xxxxxxxx
UpgradeMode       : Auto

```

<span data-ttu-id="4d121-115">이 명령은 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 클라우드 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-115">This command gets cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="4d121-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d121-116">PARAMETERS</span></span>

### <span data-ttu-id="4d121-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d121-117">-DefaultProfile</span></span>
<span data-ttu-id="4d121-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d121-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d121-119">-InputObject</span></span>
<span data-ttu-id="4d121-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4d121-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4d121-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4d121-121">-Name</span></span>
<span data-ttu-id="4d121-122">클라우드 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d121-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d121-123">-ResourceGroupName</span></span>
<span data-ttu-id="4d121-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d121-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d121-125">-SubscriptionId</span></span>
<span data-ttu-id="4d121-126">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4d121-127">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d121-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d121-128">CommonParameters</span></span>
<span data-ttu-id="4d121-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d121-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d121-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d121-131">입력</span><span class="sxs-lookup"><span data-stu-id="4d121-131">INPUTS</span></span>

### <span data-ttu-id="4d121-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="4d121-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="4d121-133">출력</span><span class="sxs-lookup"><span data-stu-id="4d121-133">OUTPUTS</span></span>

### <span data-ttu-id="4d121-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="4d121-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="4d121-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d121-135">NOTES</span></span>

<span data-ttu-id="4d121-136">별칭</span><span class="sxs-lookup"><span data-stu-id="4d121-136">ALIASES</span></span>

<span data-ttu-id="4d121-137">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4d121-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d121-138">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d121-139">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d121-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d121-140">INPUTOBJECT: <ICloudServiceIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4d121-140">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d121-141">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="4d121-141">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="4d121-142">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4d121-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d121-143">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="4d121-143">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="4d121-144">`[RoleInstanceName <String>]`: 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-144">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="4d121-145">`[RoleName <String>]`: 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-145">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="4d121-146">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4d121-147">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4d121-148">`[UpdateDomain <Int32?>]`: 업데이트 도메인을 식별하는 정수 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-148">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="4d121-149">업데이트 도메인은 0부터 시작하여 식별됩니다. 첫 번째 업데이트 도메인의 ID는 0이고, 두 번째 도메인은 ID가 1인 등입니다.</span><span class="sxs-lookup"><span data-stu-id="4d121-149">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="4d121-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d121-150">RELATED LINKS</span></span>

