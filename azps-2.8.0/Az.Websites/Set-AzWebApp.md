---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4e4e842605b883b97d408d36929bedc5fef21e4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874218"
---
# <span data-ttu-id="f5e5c-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5e5c-101">Set-AzWebApp</span></span>

## <span data-ttu-id="f5e5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e5c-103">Azure Web App을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="f5e5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5e5c-104">SYNTAX</span></span>

### <span data-ttu-id="f5e5c-105">S1</span><span class="sxs-lookup"><span data-stu-id="f5e5c-105">S1</span></span>
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

### <span data-ttu-id="f5e5c-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="f5e5c-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5e5c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f5e5c-107">DESCRIPTION</span></span>
<span data-ttu-id="f5e5c-108">**AzWebApp** Cmdlet은 Azure 웹 앱을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="f5e5c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f5e5c-109">EXAMPLES</span></span>

### <span data-ttu-id="f5e5c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5e5c-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="f5e5c-111">이 명령은 리소스 그룹 Default-웹용 WestUS와 관련 된 웹 앱 ContosoWebApp 연결 된 appservice 계획을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="f5e5c-112">링크를 사용 하 여 appservice 계획 및 관련 제약 조건을 변경 하는 방법에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="f5e5c-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="f5e5c-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="f5e5c-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f5e5c-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="f5e5c-115">이 명령은 리소스 그룹 Default-웹에 연결 된 웹 앱 ContosoWebApp에 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="f5e5c-116">변수</span><span class="sxs-lookup"><span data-stu-id="f5e5c-116">PARAMETERS</span></span>

### <span data-ttu-id="f5e5c-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f5e5c-117">-AppServicePlan</span></span>
<span data-ttu-id="f5e5c-118">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="f5e5c-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="f5e5c-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="f5e5c-119">-AppSettings</span></span>
<span data-ttu-id="f5e5c-120">앱 설정 테이블.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-120">App Settings HashTable.</span></span> <span data-ttu-id="f5e5c-121">기존 앱 설정이 바뀌고 제공 되지 않은 설정은 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="f5e5c-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5e5c-122">-AsJob</span></span>
<span data-ttu-id="f5e5c-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f5e5c-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5e5c-124">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="f5e5c-124">-AssignIdentity</span></span>
<span data-ttu-id="f5e5c-125">기존 azure web app 또는 functionapp에서 MSI 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="f5e5c-125">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="f5e5c-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="f5e5c-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="f5e5c-127">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="f5e5c-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="f5e5c-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="f5e5c-128">-AzureStoragePath</span></span>
<span data-ttu-id="f5e5c-129">컨테이너에 대 한 웹 앱 내에 탑재 하는 Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="f5e5c-130">New-AzureRmWebAppAzureStoragePath를 사용 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="f5e5c-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="f5e5c-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="f5e5c-131">-ConnectionStrings</span></span>
<span data-ttu-id="f5e5c-132">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="f5e5c-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="f5e5c-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="f5e5c-133">-ContainerImageName</span></span>
<span data-ttu-id="f5e5c-134">컨테이너 이미지 이름</span><span class="sxs-lookup"><span data-stu-id="f5e5c-134">Container Image Name</span></span>

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

### <span data-ttu-id="f5e5c-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="f5e5c-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="f5e5c-136">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="f5e5c-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="f5e5c-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="f5e5c-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="f5e5c-138">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="f5e5c-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="f5e5c-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="f5e5c-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="f5e5c-140">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="f5e5c-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="f5e5c-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="f5e5c-141">-DefaultDocuments</span></span>
<span data-ttu-id="f5e5c-142">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="f5e5c-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="f5e5c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e5c-143">-DefaultProfile</span></span>
<span data-ttu-id="f5e5c-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5e5c-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="f5e5c-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="f5e5c-146">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="f5e5c-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="f5e5c-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="f5e5c-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="f5e5c-148">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="f5e5c-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="f5e5c-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="f5e5c-149">-HandlerMappings</span></span>
<span data-ttu-id="f5e5c-150">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="f5e5c-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="f5e5c-151">-호스트 이름</span><span class="sxs-lookup"><span data-stu-id="f5e5c-151">-HostNames</span></span>
<span data-ttu-id="f5e5c-152">Web app 호스트 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="f5e5c-152">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="f5e5c-153">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="f5e5c-153">-HttpLoggingEnabled</span></span>
<span data-ttu-id="f5e5c-154">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="f5e5c-154">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="f5e5c-155">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f5e5c-155">-HttpsOnly</span></span>
<span data-ttu-id="f5e5c-156">기존 azure web app 또는 functionapp에서 HTTPS로 모든 트래픽 리디렉션 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="f5e5c-156">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="f5e5c-157">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="f5e5c-157">-ManagedPipelineMode</span></span>
<span data-ttu-id="f5e5c-158">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="f5e5c-158">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="f5e5c-159">-이름</span><span class="sxs-lookup"><span data-stu-id="f5e5c-159">-Name</span></span>
<span data-ttu-id="f5e5c-160">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="f5e5c-160">WebApp Name</span></span>

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

### <span data-ttu-id="f5e5c-161">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="f5e5c-161">-NetFrameworkVersion</span></span>
<span data-ttu-id="f5e5c-162">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="f5e5c-162">Net Framework Version</span></span>

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

### <span data-ttu-id="f5e5c-163">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="f5e5c-163">-NumberOfWorkers</span></span>
<span data-ttu-id="f5e5c-164">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-164">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="f5e5c-165">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="f5e5c-165">-PhpVersion</span></span>
<span data-ttu-id="f5e5c-166">Php 버전</span><span class="sxs-lookup"><span data-stu-id="f5e5c-166">Php Version</span></span>

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

### <span data-ttu-id="f5e5c-167">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="f5e5c-167">-RequestTracingEnabled</span></span>
<span data-ttu-id="f5e5c-168">요청 추적 사용</span><span class="sxs-lookup"><span data-stu-id="f5e5c-168">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="f5e5c-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e5c-169">-ResourceGroupName</span></span>
<span data-ttu-id="f5e5c-170">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f5e5c-170">Resource Group Name</span></span>

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

### <span data-ttu-id="f5e5c-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="f5e5c-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="f5e5c-172">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="f5e5c-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="f5e5c-173">-Web app</span><span class="sxs-lookup"><span data-stu-id="f5e5c-173">-WebApp</span></span>
<span data-ttu-id="f5e5c-174">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="f5e5c-174">WebApp Object</span></span>

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

### <span data-ttu-id="f5e5c-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="f5e5c-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="f5e5c-176">WebSocketsEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="f5e5c-176">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="f5e5c-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e5c-177">CommonParameters</span></span>
<span data-ttu-id="f5e5c-178">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e5c-179">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e5c-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e5c-180">입력</span><span class="sxs-lookup"><span data-stu-id="f5e5c-180">INPUTS</span></span>

### <span data-ttu-id="f5e5c-181">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-181">System.Int32</span></span>

### <span data-ttu-id="f5e5c-182">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f5e5c-182">System.String</span></span>

### <span data-ttu-id="f5e5c-183">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f5e5c-184">출력</span><span class="sxs-lookup"><span data-stu-id="f5e5c-184">OUTPUTS</span></span>

### <span data-ttu-id="f5e5c-185">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="f5e5c-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f5e5c-186">상속자</span><span class="sxs-lookup"><span data-stu-id="f5e5c-186">NOTES</span></span>

## <span data-ttu-id="f5e5c-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5e5c-187">RELATED LINKS</span></span>

[<span data-ttu-id="f5e5c-188">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5e5c-188">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="f5e5c-189">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5e5c-189">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="f5e5c-190">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5e5c-190">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="f5e5c-191">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5e5c-191">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="f5e5c-192">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5e5c-192">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="f5e5c-193">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5e5c-193">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
