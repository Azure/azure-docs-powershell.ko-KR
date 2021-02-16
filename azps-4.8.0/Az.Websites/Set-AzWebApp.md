---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 46c5dae54bf4f59556e62256797a43221d0650b7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412353"
---
# <span data-ttu-id="9eb2b-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9eb2b-101">Set-AzWebApp</span></span>

## <span data-ttu-id="9eb2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eb2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb2b-103">Azure 웹앱을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="9eb2b-104">구문</span><span class="sxs-lookup"><span data-stu-id="9eb2b-104">SYNTAX</span></span>

### <span data-ttu-id="9eb2b-105">S1</span><span class="sxs-lookup"><span data-stu-id="9eb2b-105">S1</span></span>
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
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eb2b-106">S2</span><span class="sxs-lookup"><span data-stu-id="9eb2b-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eb2b-107">설명</span><span class="sxs-lookup"><span data-stu-id="9eb2b-107">DESCRIPTION</span></span>
<span data-ttu-id="9eb2b-108">**Set-AzWebApp** cmdlet은 Azure 웹앱을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="9eb2b-109">예제</span><span class="sxs-lookup"><span data-stu-id="9eb2b-109">EXAMPLES</span></span>

### <span data-ttu-id="9eb2b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9eb2b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="9eb2b-111">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 웹앱 ContosoWebApp과 연결된 appservice 계획을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="9eb2b-112">이 링크를 사용하여 연결된 AppService 계획 및 제약 조건 변경에 대해 자세히 알아보면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="9eb2b-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="9eb2b-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="9eb2b-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9eb2b-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="9eb2b-115">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 웹앱 ContosoWebApp에 대해 HttpLoggingEnabled를 true로 설정</span><span class="sxs-lookup"><span data-stu-id="9eb2b-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="9eb2b-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="9eb2b-116">Example 3</span></span>

<span data-ttu-id="9eb2b-117">Azure 웹앱을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="9eb2b-118">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="9eb2b-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="9eb2b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eb2b-119">PARAMETERS</span></span>

### <span data-ttu-id="9eb2b-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="9eb2b-120">-AlwaysOn</span></span>
<span data-ttu-id="9eb2b-121">웹앱이 유휴된 후 언로드되지 않고 항상 로드되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="9eb2b-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9eb2b-122">-AppServicePlan</span></span>
<span data-ttu-id="9eb2b-123">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="9eb2b-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="9eb2b-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="9eb2b-124">-AppSettings</span></span>
<span data-ttu-id="9eb2b-125">앱 설정 해시테이블.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-125">App Settings HashTable.</span></span> <span data-ttu-id="9eb2b-126">기존 앱 설정이 대체됩니다. 이 설정은 제공되지 않은 모든 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="9eb2b-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9eb2b-127">-AsJob</span></span>
<span data-ttu-id="9eb2b-128">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9eb2b-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9eb2b-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9eb2b-129">-AssignIdentity</span></span>
<span data-ttu-id="9eb2b-130">기존 azure webapp 또는 functionapp에서 MSI 사용/사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="9eb2b-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="9eb2b-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="9eb2b-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="9eb2b-132">자동 교환의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="9eb2b-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="9eb2b-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="9eb2b-133">-AzureStoragePath</span></span>
<span data-ttu-id="9eb2b-134">Web App for Container 내부에 탑재할 Azure Storage입니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="9eb2b-135">이 New-AzureRmWebAppAzureStoragePath 사용하여 만들기</span><span class="sxs-lookup"><span data-stu-id="9eb2b-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="9eb2b-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="9eb2b-136">-ConnectionStrings</span></span>
<span data-ttu-id="9eb2b-137">연결 문자열 해시Table</span><span class="sxs-lookup"><span data-stu-id="9eb2b-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="9eb2b-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="9eb2b-138">-ContainerImageName</span></span>
<span data-ttu-id="9eb2b-139">컨테이너 이미지 이름</span><span class="sxs-lookup"><span data-stu-id="9eb2b-139">Container Image Name</span></span>

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

### <span data-ttu-id="9eb2b-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="9eb2b-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="9eb2b-141">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="9eb2b-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="9eb2b-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="9eb2b-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="9eb2b-143">개인 컨테이너 레지스트리 서버 URL</span><span class="sxs-lookup"><span data-stu-id="9eb2b-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="9eb2b-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="9eb2b-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="9eb2b-145">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="9eb2b-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="9eb2b-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="9eb2b-146">-DefaultDocuments</span></span>
<span data-ttu-id="9eb2b-147">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="9eb2b-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="9eb2b-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb2b-148">-DefaultProfile</span></span>
<span data-ttu-id="9eb2b-149">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eb2b-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9eb2b-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="9eb2b-151">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="9eb2b-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="9eb2b-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="9eb2b-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="9eb2b-153">컨테이너 연속 배포 웹후크를 활성화/비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="9eb2b-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="9eb2b-154">-FtpsState</span></span>
<span data-ttu-id="9eb2b-155">앱에 대한 Ftps 상태 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="9eb2b-156">허용되는 값 [AllAllowed | 사용 안 | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="9eb2b-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="9eb2b-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="9eb2b-157">-HandlerMappings</span></span>
<span data-ttu-id="9eb2b-158">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="9eb2b-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="9eb2b-159">-HostNames</span><span class="sxs-lookup"><span data-stu-id="9eb2b-159">-HostNames</span></span>
<span data-ttu-id="9eb2b-160">WebApp HostNames 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="9eb2b-160">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="9eb2b-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9eb2b-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="9eb2b-162">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="9eb2b-162">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="9eb2b-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9eb2b-163">-HttpsOnly</span></span>
<span data-ttu-id="9eb2b-164">기존 Azure 웹앱 또는 functionapp에서 HTTPS로 모든 트래픽 리디렉션 사용/사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="9eb2b-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="9eb2b-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="9eb2b-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="9eb2b-166">관리되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="9eb2b-166">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="9eb2b-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="9eb2b-167">-MinTlsVersion</span></span>
<span data-ttu-id="9eb2b-168">SSL 요청에 필요한 TLS의 최소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="9eb2b-169">허용되는 값 [1.0 | 1.1 | 1.2].</span><span class="sxs-lookup"><span data-stu-id="9eb2b-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="9eb2b-170">-Name</span><span class="sxs-lookup"><span data-stu-id="9eb2b-170">-Name</span></span>
<span data-ttu-id="9eb2b-171">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="9eb2b-171">WebApp Name</span></span>

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

### <span data-ttu-id="9eb2b-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="9eb2b-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="9eb2b-173">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="9eb2b-173">Net Framework Version</span></span>

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

### <span data-ttu-id="9eb2b-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="9eb2b-174">-NumberOfWorkers</span></span>
<span data-ttu-id="9eb2b-175">할당할 작업자 수</span><span class="sxs-lookup"><span data-stu-id="9eb2b-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="9eb2b-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="9eb2b-176">-PhpVersion</span></span>
<span data-ttu-id="9eb2b-177">Php 버전</span><span class="sxs-lookup"><span data-stu-id="9eb2b-177">Php Version</span></span>

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

### <span data-ttu-id="9eb2b-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="9eb2b-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="9eb2b-179">요청 추적 사용</span><span class="sxs-lookup"><span data-stu-id="9eb2b-179">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="9eb2b-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eb2b-180">-ResourceGroupName</span></span>
<span data-ttu-id="9eb2b-181">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9eb2b-181">Resource Group Name</span></span>

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

### <span data-ttu-id="9eb2b-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="9eb2b-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="9eb2b-183">32비트 Worker 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="9eb2b-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="9eb2b-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9eb2b-184">-WebApp</span></span>
<span data-ttu-id="9eb2b-185">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="9eb2b-185">WebApp Object</span></span>

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

### <span data-ttu-id="9eb2b-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="9eb2b-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="9eb2b-187">WebSocketsEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="9eb2b-187">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="9eb2b-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb2b-188">CommonParameters</span></span>
<span data-ttu-id="9eb2b-189">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb2b-190">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb2b-191">입력</span><span class="sxs-lookup"><span data-stu-id="9eb2b-191">INPUTS</span></span>

### <span data-ttu-id="9eb2b-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9eb2b-192">System.Int32</span></span>

### <span data-ttu-id="9eb2b-193">System.String</span><span class="sxs-lookup"><span data-stu-id="9eb2b-193">System.String</span></span>

### <span data-ttu-id="9eb2b-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="9eb2b-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9eb2b-195">출력</span><span class="sxs-lookup"><span data-stu-id="9eb2b-195">OUTPUTS</span></span>

### <span data-ttu-id="9eb2b-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="9eb2b-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9eb2b-197">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9eb2b-197">NOTES</span></span>
<span data-ttu-id="9eb2b-198">아래 제공된 cmdlet은 AZURE 웹앱을 **DOTNETCORE로 업데이트하는 데 도움이 됩니다.**</span><span class="sxs-lookup"><span data-stu-id="9eb2b-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="9eb2b-199">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="9eb2b-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="9eb2b-200">Default-Web-WestUS의 값을 웹앱의 리소스 그룹 이름으로 바꾸고 ContosoWebApp을 웹앱 이름으로 바 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="9eb2b-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="9eb2b-201">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9eb2b-201">RELATED LINKS</span></span>

[<span data-ttu-id="9eb2b-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9eb2b-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="9eb2b-203">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9eb2b-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="9eb2b-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9eb2b-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="9eb2b-205">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9eb2b-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="9eb2b-206">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9eb2b-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="9eb2b-207">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9eb2b-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

