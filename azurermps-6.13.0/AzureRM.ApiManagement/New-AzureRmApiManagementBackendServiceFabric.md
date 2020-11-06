---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
ms.openlocfilehash: 925e4949b444c9338fad3f88cf5066430e1b5a75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528682"
---
# <span data-ttu-id="a7d6c-101">New-AzureRmApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7d6c-101">New-AzureRmApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="a7d6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d6c-103">의 개체를 만듭니다. `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="a7d6c-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7d6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7d6c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint <String[]>
 -ClientCertificateThumbprint <String> [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>]
 [-ServerCertificateThumbprint <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7d6c-105">DESCRIPTION</span></span>

<span data-ttu-id="a7d6c-106">**AzureRmApiManagementBackendServiceFabric** cmdlet은 `PsApiManagementServiceFabric` Cmdlet **New-AzureRmApiManagementBackend** 및 **Set-AzureRmApiManagementBackend** 에 사용할 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-106">The **New-AzureRmApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzureRmApiManagementBackend** and **Set-AzureRmApiManagementBackend**.</span></span>

## <span data-ttu-id="a7d6c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a7d6c-107">EXAMPLES</span></span>

### <span data-ttu-id="a7d6c-108">예제 1: 백엔드 서비스 패브릭 In-Memory 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="a7d6c-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="a7d6c-109">백 엔드 서비스 패브릭 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="a7d6c-110">변수</span><span class="sxs-lookup"><span data-stu-id="a7d6c-110">PARAMETERS</span></span>

### <span data-ttu-id="a7d6c-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="a7d6c-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="a7d6c-112">관리 끝점에 대 한 클라이언트 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="a7d6c-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a7d6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d6c-114">-DefaultProfile</span></span>
<span data-ttu-id="a7d6c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7d6c-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7d6c-116">-ManagementEndpoint</span></span>
<span data-ttu-id="a7d6c-117">서비스 패브릭 클러스터 관리 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="a7d6c-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a7d6c-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="a7d6c-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="a7d6c-120">서비스 패브릭 파티션을 확인할 때 최대 다시 시도 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="a7d6c-121">이 매개 변수는 선택 사항이 며 기본값은 5입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="a7d6c-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="a7d6c-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="a7d6c-123">클러스터 관리 서비스에서 tls 통신에 사용 하는 인증서의 지문입니다. 이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="a7d6c-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="a7d6c-124">-ServerX509Name</span></span>
<span data-ttu-id="a7d6c-125">서버 X509 인증서 이름 컬렉션</span><span class="sxs-lookup"><span data-stu-id="a7d6c-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="a7d6c-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="a7d6c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d6c-127">CommonParameters</span></span>
<span data-ttu-id="a7d6c-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d6c-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d6c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d6c-130">입력</span><span class="sxs-lookup"><span data-stu-id="a7d6c-130">INPUTS</span></span>

### <span data-ttu-id="a7d6c-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a7d6c-131">System.String</span></span>

## <span data-ttu-id="a7d6c-132">출력</span><span class="sxs-lookup"><span data-stu-id="a7d6c-132">OUTPUTS</span></span>

### <span data-ttu-id="a7d6c-133">ApiManagement. ServiceManagement. \ PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7d6c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="a7d6c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="a7d6c-134">NOTES</span></span>

## <span data-ttu-id="a7d6c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7d6c-135">RELATED LINKS</span></span>

[<span data-ttu-id="a7d6c-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a7d6c-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="a7d6c-137">새로운 AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a7d6c-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a7d6c-138">새로운 AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a7d6c-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="a7d6c-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a7d6c-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a7d6c-140">제거-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a7d6c-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
