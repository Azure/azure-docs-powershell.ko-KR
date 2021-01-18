---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: 3101ca2b120860dfa6df95786e235fc88fd0fc78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496133"
---
# <span data-ttu-id="155a6-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="155a6-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="155a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="155a6-102">SYNOPSIS</span></span>
<span data-ttu-id="155a6-103">CommunicationService 및 해당 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="155a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="155a6-104">SYNTAX</span></span>

### <span data-ttu-id="155a6-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="155a6-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="155a6-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="155a6-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="155a6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="155a6-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="155a6-108">List1</span><span class="sxs-lookup"><span data-stu-id="155a6-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="155a6-109">설명</span><span class="sxs-lookup"><span data-stu-id="155a6-109">DESCRIPTION</span></span>
<span data-ttu-id="155a6-110">CommunicationService 및 해당 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="155a6-111">예제</span><span class="sxs-lookup"><span data-stu-id="155a6-111">EXAMPLES</span></span>

### <span data-ttu-id="155a6-112">예제 1: 구독에 대한 기존 CommunicationServices 나열</span><span class="sxs-lookup"><span data-stu-id="155a6-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="155a6-113">해당 구독의 모든 ACS 리소스 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="155a6-114">예제 2: 지정된 Azure Communication 리소스에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="155a6-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="155a6-115">일치하는 제공된 매개 변수가 있는 경우 ACS 리소스에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="155a6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="155a6-116">PARAMETERS</span></span>

### <span data-ttu-id="155a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="155a6-117">-DefaultProfile</span></span>
<span data-ttu-id="155a6-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="155a6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="155a6-119">-InputObject</span></span>
<span data-ttu-id="155a6-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="155a6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="155a6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="155a6-121">-Name</span></span>
<span data-ttu-id="155a6-122">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-122">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="155a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="155a6-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="155a6-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="155a6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="155a6-126">-SubscriptionId</span></span>
<span data-ttu-id="155a6-127">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="155a6-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="155a6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="155a6-129">CommonParameters</span></span>
<span data-ttu-id="155a6-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="155a6-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="155a6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="155a6-132">입력</span><span class="sxs-lookup"><span data-stu-id="155a6-132">INPUTS</span></span>

### <span data-ttu-id="155a6-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="155a6-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="155a6-134">출력</span><span class="sxs-lookup"><span data-stu-id="155a6-134">OUTPUTS</span></span>

### <span data-ttu-id="155a6-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="155a6-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="155a6-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="155a6-136">NOTES</span></span>

<span data-ttu-id="155a6-137">별칭</span><span class="sxs-lookup"><span data-stu-id="155a6-137">ALIASES</span></span>

<span data-ttu-id="155a6-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="155a6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="155a6-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="155a6-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="155a6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="155a6-141">INPUTOBJECT: <ICommunicationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="155a6-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="155a6-142">`[CommunicationServiceName <String>]`: CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="155a6-143">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="155a6-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="155a6-144">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="155a6-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="155a6-145">`[OperationId <String>]`: 진행 중 비동기 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="155a6-146">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="155a6-147">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="155a6-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="155a6-149">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="155a6-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="155a6-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="155a6-150">RELATED LINKS</span></span>

