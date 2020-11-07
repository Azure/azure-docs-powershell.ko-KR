---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 7fb1118d612aae7cf5495f0743550510088e5dbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698298"
---
# <span data-ttu-id="d4fc0-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4fc0-101">Set-AzWebApp</span></span>



## <span data-ttu-id="d4fc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4fc0-102">SYNOPSIS</span></span>

<span data-ttu-id="d4fc0-103">Azure Web App을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-103">Modifies an Azure Web App.</span></span>



## <span data-ttu-id="d4fc0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4fc0-104">SYNTAX</span></span>



### <span data-ttu-id="d4fc0-105">S1</span><span class="sxs-lookup"><span data-stu-id="d4fc0-105">S1</span></span>

```

Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]

 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]

 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]

 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]

 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]

 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]

 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]

 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]

 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]

 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



### <span data-ttu-id="d4fc0-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="d4fc0-106">S2</span></span>

```

Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]

 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



## <span data-ttu-id="d4fc0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d4fc0-107">DESCRIPTION</span></span>

<span data-ttu-id="d4fc0-108">**AzWebApp** Cmdlet은 Azure 웹 앱을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>



## <span data-ttu-id="d4fc0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d4fc0-109">EXAMPLES</span></span>



### <span data-ttu-id="d4fc0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d4fc0-110">Example 1</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"

```



<span data-ttu-id="d4fc0-111">이 명령은 리소스 그룹 Default-웹용 WestUS와 관련 된 웹 앱 ContosoWebApp 연결 된 appservice 계획을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="d4fc0-112">링크를 사용 하 여 관련 된 appservice 계획 및 제약 조건을 변경 하는 방법에 대 한 자세한 learm.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>

https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan


### <span data-ttu-id="d4fc0-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d4fc0-113">Example 2</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true

```



<span data-ttu-id="d4fc0-114">이 명령은 리소스 그룹 Default-웹에 연결 된 웹 앱 ContosoWebApp에 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-114">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>



## <span data-ttu-id="d4fc0-115">변수</span><span class="sxs-lookup"><span data-stu-id="d4fc0-115">PARAMETERS</span></span>



### <span data-ttu-id="d4fc0-116">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d4fc0-116">-AppServicePlan</span></span>

<span data-ttu-id="d4fc0-117">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="d4fc0-117">App Service Plan Name</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: 2

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-118">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="d4fc0-118">-AppSettings</span></span>

<span data-ttu-id="d4fc0-119">앱 설정 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="d4fc0-119">App Settings HashTable</span></span>



```yaml

Type: System.Collections.Hashtable

Parameter Sets: S1

Aliases:



Required: False

Position: 9

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4fc0-120">-AsJob</span></span>

<span data-ttu-id="d4fc0-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d4fc0-121">Run cmdlet in the background</span></span>



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



### <span data-ttu-id="d4fc0-122">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="d4fc0-122">-AssignIdentity</span></span>

<span data-ttu-id="d4fc0-123">기존 azure web app 또는 functionapp에서 MSI 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="d4fc0-123">Enable/disable MSI on an existing azure webapp or functionapp</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-124">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="d4fc0-124">-AutoSwapSlotName</span></span>

<span data-ttu-id="d4fc0-125">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="d4fc0-125">Destination slot name for auto swap</span></span>



```yaml

Type: System.String

Parameter Sets: (All)

Aliases:



Required: False

Position: 15

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-126">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="d4fc0-126">-AzureStoragePath</span></span>

<span data-ttu-id="d4fc0-127">컨테이너에 대 한 웹 앱 내에 탑재 하는 Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-127">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="d4fc0-128">New-AzureRmWebAppAzureStoragePath를 사용 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="d4fc0-128">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>



```yaml

Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-129">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="d4fc0-129">-ConnectionStrings</span></span>

<span data-ttu-id="d4fc0-130">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="d4fc0-130">Connection Strings HashTable</span></span>



```yaml

Type: System.Collections.Hashtable

Parameter Sets: S1

Aliases:



Required: False

Position: 10

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-131">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="d4fc0-131">-ContainerImageName</span></span>

<span data-ttu-id="d4fc0-132">컨테이너 이미지 이름</span><span class="sxs-lookup"><span data-stu-id="d4fc0-132">Container Image Name</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-133">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="d4fc0-133">-ContainerRegistryPassword</span></span>

<span data-ttu-id="d4fc0-134">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="d4fc0-134">Private Container Registry Password</span></span>



```yaml

Type: System.Security.SecureString

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-135">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="d4fc0-135">-ContainerRegistryUrl</span></span>

<span data-ttu-id="d4fc0-136">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="d4fc0-136">Private Container Registry Server Url</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-137">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="d4fc0-137">-ContainerRegistryUser</span></span>

<span data-ttu-id="d4fc0-138">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="d4fc0-138">Private Container Registry Username</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-139">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="d4fc0-139">-DefaultDocuments</span></span>

<span data-ttu-id="d4fc0-140">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="d4fc0-140">Default Documents String Array</span></span>



```yaml

Type: System.String[]

Parameter Sets: S1

Aliases:



Required: False

Position: 3

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4fc0-141">-DefaultProfile</span></span>

<span data-ttu-id="d4fc0-142">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>



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



### <span data-ttu-id="d4fc0-143">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d4fc0-143">-DetailedErrorLoggingEnabled</span></span>

<span data-ttu-id="d4fc0-144">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="d4fc0-144">Detailed Error Logging Enabled Boolean</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 8

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-145">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="d4fc0-145">-EnableContainerContinuousDeployment</span></span>

<span data-ttu-id="d4fc0-146">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="d4fc0-146">Enables/Disables container continuous deployment webhook</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-147">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="d4fc0-147">-HandlerMappings</span></span>

<span data-ttu-id="d4fc0-148">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="d4fc0-148">Handler Mappings IList</span></span>



```yaml

Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]

Parameter Sets: S1

Aliases:



Required: False

Position: 11

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-149">-호스트 이름</span><span class="sxs-lookup"><span data-stu-id="d4fc0-149">-HostNames</span></span>

<span data-ttu-id="d4fc0-150">Web app 호스트 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="d4fc0-150">WebApp HostNames String Array</span></span>



```yaml

Type: System.String[]

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d4fc0-151">-HttpLoggingEnabled</span></span>

<span data-ttu-id="d4fc0-152">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="d4fc0-152">HttpLoggingEnabled Boolean</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 7

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d4fc0-153">-HttpsOnly</span></span>

<span data-ttu-id="d4fc0-154">기존 azure web app 또는 functionapp에서 HTTPS로 모든 트래픽 리디렉션 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="d4fc0-154">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="d4fc0-155">-ManagedPipelineMode</span></span>

<span data-ttu-id="d4fc0-156">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="d4fc0-156">Managed Pipeline Mode Name</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:

Accepted values: Classic, Integrated



Required: False

Position: 12

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-157">-이름</span><span class="sxs-lookup"><span data-stu-id="d4fc0-157">-Name</span></span>

<span data-ttu-id="d4fc0-158">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="d4fc0-158">WebApp Name</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: True

Position: 1

Default value: None

Accept pipeline input: True (ByPropertyName)

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="d4fc0-159">-NetFrameworkVersion</span></span>

<span data-ttu-id="d4fc0-160">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="d4fc0-160">Net Framework Version</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: 4

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="d4fc0-161">-NumberOfWorkers</span></span>

<span data-ttu-id="d4fc0-162">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-162">The number of workers to be allocated</span></span>



```yaml

Type: System.Int32

Parameter Sets: (All)

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: True (ByValue)

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="d4fc0-163">-PhpVersion</span></span>

<span data-ttu-id="d4fc0-164">Php 버전</span><span class="sxs-lookup"><span data-stu-id="d4fc0-164">Php Version</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: 5

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="d4fc0-165">-RequestTracingEnabled</span></span>

<span data-ttu-id="d4fc0-166">요청 추적 사용</span><span class="sxs-lookup"><span data-stu-id="d4fc0-166">Request Tracing Enabled</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 6

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4fc0-167">-ResourceGroupName</span></span>

<span data-ttu-id="d4fc0-168">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d4fc0-168">Resource Group Name</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: True

Position: 0

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-169">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="d4fc0-169">-Use32BitWorkerProcess</span></span>

<span data-ttu-id="d4fc0-170">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="d4fc0-170">Use 32-bit Worker Process Boolean</span></span>



```yaml

Type: System.Boolean

Parameter Sets: (All)

Aliases:



Required: False

Position: 14

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-171">-Web app</span><span class="sxs-lookup"><span data-stu-id="d4fc0-171">-WebApp</span></span>

<span data-ttu-id="d4fc0-172">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="d4fc0-172">WebApp Object</span></span>



```yaml

Type: Microsoft.Azure.Commands.WebApps.Models.PSSite

Parameter Sets: S2

Aliases:



Required: True

Position: 0

Default value: None

Accept pipeline input: True (ByValue)

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-173">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="d4fc0-173">-WebSocketsEnabled</span></span>

<span data-ttu-id="d4fc0-174">WebSocketsEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="d4fc0-174">WebSocketsEnabled Boolean</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 13

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="d4fc0-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4fc0-175">CommonParameters</span></span>

<span data-ttu-id="d4fc0-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4fc0-177">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4fc0-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>



## <span data-ttu-id="d4fc0-178">입력</span><span class="sxs-lookup"><span data-stu-id="d4fc0-178">INPUTS</span></span>



### <span data-ttu-id="d4fc0-179">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-179">System.Int32</span></span>



### <span data-ttu-id="d4fc0-180">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d4fc0-180">System.String</span></span>



### <span data-ttu-id="d4fc0-181">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-181">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="d4fc0-182">출력</span><span class="sxs-lookup"><span data-stu-id="d4fc0-182">OUTPUTS</span></span>



### <span data-ttu-id="d4fc0-183">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="d4fc0-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="d4fc0-184">상속자</span><span class="sxs-lookup"><span data-stu-id="d4fc0-184">NOTES</span></span>



## <span data-ttu-id="d4fc0-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4fc0-185">RELATED LINKS</span></span>



[<span data-ttu-id="d4fc0-186">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4fc0-186">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



[<span data-ttu-id="d4fc0-187">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4fc0-187">New-AzWebApp</span></span>](./New-AzWebApp.md)



[<span data-ttu-id="d4fc0-188">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4fc0-188">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)



[<span data-ttu-id="d4fc0-189">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4fc0-189">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)



[<span data-ttu-id="d4fc0-190">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4fc0-190">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



[<span data-ttu-id="d4fc0-191">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4fc0-191">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

