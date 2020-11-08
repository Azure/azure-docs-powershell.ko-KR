---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnetworkstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
ms.openlocfilehash: 5ba351ab1a5102acc1855e13821650b8ce1b4373
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041930"
---
# <span data-ttu-id="d689d-101">Get-AzApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="d689d-101">Get-AzApiManagementNetworkStatus</span></span>

## <span data-ttu-id="d689d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d689d-102">SYNOPSIS</span></span>
<span data-ttu-id="d689d-103">Api Management 서비스가 클라우드 서비스 내에서 의존 하는 외부 리소스에 대 한 연결 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d689d-103">Gets the Connectivity Status to the external resources on which the Api Management service depends from inside the Cloud Service.</span></span> <span data-ttu-id="d689d-104">이렇게 하면 DNS 서버가 CloudService에 표시 되는 것으로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d689d-104">This also returns the DNS Servers as visible to the CloudService.</span></span>

## <span data-ttu-id="d689d-105">구문과</span><span class="sxs-lookup"><span data-stu-id="d689d-105">SYNTAX</span></span>

### <span data-ttu-id="d689d-106">ByInputObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="d689d-106">ByInputObject (Default)</span></span>
```
Get-AzApiManagementNetworkStatus -ApiManagementObject <PsApiManagement> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d689d-107">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="d689d-107">ExpandedParameter</span></span>
```
Get-AzApiManagementNetworkStatus -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d689d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d689d-108">DESCRIPTION</span></span>
<span data-ttu-id="d689d-109">Api Management 서비스의 네트워크 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d689d-109">Gets the Network status of their Api Management service</span></span>

## <span data-ttu-id="d689d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d689d-110">EXAMPLES</span></span>

### <span data-ttu-id="d689d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d689d-111">Example 1</span></span>
```powershell
PS D:\github\azure-powershell> Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice

Location DnsServers      ConnectivityStatus
-------- ----------      ------------------
West US  {168.63.129.16} {apimgmtstaoonqs7wwzjosky.blob.core.windows.net, apimgmtstaoonqs7wwzjosky.file.core.windows.net, apimgmtstaoonqs7wwzjosky.queue.core.windows.net, apimgmtstaoonqs7wwzjosk...


PS D:\github\azure-powershell> $networkStatus = Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice
PS D:\github\azure-powershell> $networkStatus.ConnectivityStatus


Name             : apimgmtstaoonqs7wwzjosky.blob.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : apimgmtstaoonqs7wwzjosky.file.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.queue.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.table.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : bx9gltecfv.database.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:41 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : https://prod3.metrics.nsatc.net:1886/RecoveryService
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:07:11 PM
LastStatusChange : 4/29/2019 1:31:30 PM

Name             : prod.warmpath.msftcloudes.com
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : Scm
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:04:27 PM
LastStatusChange : 4/30/2019 11:16:20 PM
```

<span data-ttu-id="d689d-112">ApiManagement 서비스에 종속 되는 여러 리소스의 연결 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d689d-112">Gets the connectivity status of the different resources on which ApiManagement service depends upon.</span></span>

## <span data-ttu-id="d689d-113">변수</span><span class="sxs-lookup"><span data-stu-id="d689d-113">PARAMETERS</span></span>

### <span data-ttu-id="d689d-114">-ApiManagementObject</span><span class="sxs-lookup"><span data-stu-id="d689d-114">-ApiManagementObject</span></span>
<span data-ttu-id="d689d-115">PsApiManagement의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="d689d-115">Instance of PsApiManagement.</span></span> <span data-ttu-id="d689d-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d689d-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d689d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d689d-117">-DefaultProfile</span></span>
<span data-ttu-id="d689d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d689d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d689d-119">-위치</span><span class="sxs-lookup"><span data-stu-id="d689d-119">-Location</span></span>
<span data-ttu-id="d689d-120">API Management 서비스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d689d-120">Location of the API Management Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d689d-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d689d-121">-Name</span></span>
<span data-ttu-id="d689d-122">API Management의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d689d-122">Name of API Management.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d689d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d689d-123">-ResourceGroupName</span></span>
<span data-ttu-id="d689d-124">API Management가 존재 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d689d-124">Name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d689d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d689d-125">CommonParameters</span></span>
<span data-ttu-id="d689d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d689d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d689d-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d689d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d689d-128">입력</span><span class="sxs-lookup"><span data-stu-id="d689d-128">INPUTS</span></span>

### <span data-ttu-id="d689d-129">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="d689d-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="d689d-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d689d-130">System.String</span></span>

## <span data-ttu-id="d689d-131">출력</span><span class="sxs-lookup"><span data-stu-id="d689d-131">OUTPUTS</span></span>

### <span data-ttu-id="d689d-132">ApiManagement. PsApiManagementNetworkStatus/.</span><span class="sxs-lookup"><span data-stu-id="d689d-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span></span>

## <span data-ttu-id="d689d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="d689d-133">NOTES</span></span>

## <span data-ttu-id="d689d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d689d-134">RELATED LINKS</span></span>
