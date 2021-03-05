---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportproblemclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
ms.openlocfilehash: 0c8bf7d7a8217ed63920495591f8ad061f1b0a8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972496"
---
# <span data-ttu-id="eda6b-101">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="eda6b-101">Get-AzSupportProblemClassification</span></span>

## <span data-ttu-id="eda6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eda6b-102">SYNOPSIS</span></span>
<span data-ttu-id="eda6b-103">지정된 서비스에 대한 문제 분류를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-103">Get problem classifications for the service specified.</span></span>

## <span data-ttu-id="eda6b-104">구문</span><span class="sxs-lookup"><span data-stu-id="eda6b-104">SYNTAX</span></span>

### <span data-ttu-id="eda6b-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="eda6b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportProblemClassification -ServiceId <String> [-Id <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eda6b-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eda6b-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportProblemClassification [-Id <String>] -ServiceObject <PSSupportService>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eda6b-107">설명</span><span class="sxs-lookup"><span data-stu-id="eda6b-107">DESCRIPTION</span></span>
<span data-ttu-id="eda6b-108">Azure 서비스에 대한 현재 문제 분류 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-108">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="eda6b-109">서비스 및 문제 분류 GUID를 사용하여 New-AzSupportTicket을 사용하여 새 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-109">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="eda6b-110">항상 프로그래밍으로 얻은 서비스 및 문제 분류 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-110">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="eda6b-111">이 연습을 통해 지원 티켓을 만들기 위한 최신 서비스 및 문제 분류 GUID가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-111">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="eda6b-112">예제</span><span class="sxs-lookup"><span data-stu-id="eda6b-112">EXAMPLES</span></span>

### <span data-ttu-id="eda6b-113">예제 1: 서비스 ID 매개 변수를 사용하여 서비스에 대한 모든 문제 분류자 를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-113">Example 1: Get all problem classificaitons for a service using service id parameter.</span></span>
```powershell
PS C:\> Get-AzSupportProblemClassification -ServiceId "{vm_running_windows_service_guid}"

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="eda6b-114">예제 2: 부모 서비스 개체를 사용하여 서비스에 대한 모든 문제 분류자 를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-114">Example 2: Get all problem classificaitons for a service using parent service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification 

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="eda6b-115">예제 3: 배관 서비스 개체에 의해 ID로 단일 문제 분류에 대한 세부 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-115">Example 3: Get details of a single problem classificaiton by id by piping service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification -Id 923d6b56-d573-f943-b65d-d69ba79ea21a

Name                                 DisplayName
----                                 -----------
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
```

## <span data-ttu-id="eda6b-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="eda6b-116">PARAMETERS</span></span>

### <span data-ttu-id="eda6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda6b-117">-DefaultProfile</span></span>
<span data-ttu-id="eda6b-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eda6b-119">-Id</span><span class="sxs-lookup"><span data-stu-id="eda6b-119">-Id</span></span>
<span data-ttu-id="eda6b-120">문제 분류 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-120">Problem classification id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda6b-121">-ServiceId</span><span class="sxs-lookup"><span data-stu-id="eda6b-121">-ServiceId</span></span>
<span data-ttu-id="eda6b-122">모든 문제 분류를 검색하는 서비스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-122">Service id for which all problem classifications are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda6b-123">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="eda6b-123">-ServiceObject</span></span>
<span data-ttu-id="eda6b-124">문제 분류를 검색하는 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-124">Service object for which problem classifications are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportService
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eda6b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda6b-125">CommonParameters</span></span>
<span data-ttu-id="eda6b-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eda6b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda6b-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eda6b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda6b-128">입력</span><span class="sxs-lookup"><span data-stu-id="eda6b-128">INPUTS</span></span>

### <span data-ttu-id="eda6b-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span><span class="sxs-lookup"><span data-stu-id="eda6b-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="eda6b-130">출력</span><span class="sxs-lookup"><span data-stu-id="eda6b-130">OUTPUTS</span></span>

### <span data-ttu-id="eda6b-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="eda6b-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span></span>

## <span data-ttu-id="eda6b-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eda6b-132">NOTES</span></span>

## <span data-ttu-id="eda6b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eda6b-133">RELATED LINKS</span></span>
