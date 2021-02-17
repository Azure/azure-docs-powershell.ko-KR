---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 744889e022301951bbc9ba2895eb5750f85925d0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401660"
---
# <span data-ttu-id="8ce91-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ce91-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="8ce91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ce91-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce91-103">다음의 개체를 만듭니다. `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="8ce91-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="8ce91-104">구문</span><span class="sxs-lookup"><span data-stu-id="8ce91-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ce91-105">설명</span><span class="sxs-lookup"><span data-stu-id="8ce91-105">DESCRIPTION</span></span>

<span data-ttu-id="8ce91-106">**New-AzApiManagementBackendServiceFabric** `PsApiManagementServiceFabric` cmdlet은 **New-AzApiManagementBackend** 및 **Set-AzApiManagementBackend** cmdlet에 사용할 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="8ce91-107">예제</span><span class="sxs-lookup"><span data-stu-id="8ce91-107">EXAMPLES</span></span>

### <span data-ttu-id="8ce91-108">예제 1: 백end Service Fabric 개체 In-Memory 만들기</span><span class="sxs-lookup"><span data-stu-id="8ce91-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="8ce91-109">백end Service Fabric 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="8ce91-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ce91-110">PARAMETERS</span></span>

### <span data-ttu-id="8ce91-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="8ce91-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="8ce91-112">관리 엔드포인트에 대한 클라이언트 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="8ce91-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-113">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ce91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce91-114">-DefaultProfile</span></span>
<span data-ttu-id="8ce91-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ce91-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ce91-116">-ManagementEndpoint</span></span>
<span data-ttu-id="8ce91-117">Service Fabric 클러스터 관리 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="8ce91-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-118">This parameter is required.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce91-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="8ce91-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="8ce91-120">Service Fabric 파티션을 만들 때 최대 재시도 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="8ce91-121">이 매개 변수는 선택 사항이며 기본값은 5입니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-121">This parameter is optional and default value is 5.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce91-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="8ce91-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="8ce91-123">TLS 통신에 사용하는 인증서 클러스터 관리 서비스의 지문입니다. 이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce91-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="8ce91-124">-ServerX509Name</span></span>
<span data-ttu-id="8ce91-125">서버 X509 인증서 이름 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="8ce91-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-126">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce91-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce91-127">CommonParameters</span></span>
<span data-ttu-id="8ce91-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8ce91-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce91-129">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8ce91-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce91-130">입력</span><span class="sxs-lookup"><span data-stu-id="8ce91-130">INPUTS</span></span>

### <span data-ttu-id="8ce91-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8ce91-131">System.String</span></span>

## <span data-ttu-id="8ce91-132">출력</span><span class="sxs-lookup"><span data-stu-id="8ce91-132">OUTPUTS</span></span>

### <span data-ttu-id="8ce91-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ce91-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="8ce91-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8ce91-134">NOTES</span></span>

## <span data-ttu-id="8ce91-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ce91-135">RELATED LINKS</span></span>

[<span data-ttu-id="8ce91-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8ce91-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="8ce91-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8ce91-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="8ce91-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8ce91-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="8ce91-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8ce91-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="8ce91-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8ce91-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
