---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219137"
---
# <span data-ttu-id="05a6b-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="05a6b-101">Set-AzWebApp</span></span>

## <span data-ttu-id="05a6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="05a6b-103">Azure Web App을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="05a6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05a6b-104">SYNTAX</span></span>

### <span data-ttu-id="05a6b-105">S1</span><span class="sxs-lookup"><span data-stu-id="05a6b-105">S1</span></span>
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

### <span data-ttu-id="05a6b-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="05a6b-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05a6b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="05a6b-107">DESCRIPTION</span></span>
<span data-ttu-id="05a6b-108">**AzWebApp** Cmdlet은 Azure 웹 앱을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="05a6b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="05a6b-109">EXAMPLES</span></span>

### <span data-ttu-id="05a6b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="05a6b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="05a6b-111">이 명령은 리소스 그룹 Default-웹용 WestUS와 관련 된 웹 앱 ContosoWebApp 연결 된 appservice 계획을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="05a6b-112">링크를 사용 하 여 appservice 계획 및 관련 제약 조건을 변경 하는 방법에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="05a6b-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="05a6b-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="05a6b-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="05a6b-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="05a6b-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="05a6b-115">이 명령은 리소스 그룹 Default-웹에 연결 된 웹 앱 ContosoWebApp에 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="05a6b-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="05a6b-116">Example 3</span></span>

<span data-ttu-id="05a6b-117">Azure Web App을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="05a6b-118">생성</span><span class="sxs-lookup"><span data-stu-id="05a6b-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="05a6b-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="05a6b-119">Example 4</span></span>

<span data-ttu-id="05a6b-120">다음 예제에서는 Web App ContosoWebApp myConnectionString 이라는 연결 문자열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="05a6b-121">이렇게 하면 웹 앱 ContosoWebApp의 모든 기존 연결 문자열이 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="05a6b-122">변수</span><span class="sxs-lookup"><span data-stu-id="05a6b-122">PARAMETERS</span></span>

### <span data-ttu-id="05a6b-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="05a6b-123">-AlwaysOn</span></span>
<span data-ttu-id="05a6b-124">웹 앱이 유휴 상태가 된 후에 언로드되기 전에 항상 로드 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="05a6b-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="05a6b-125">-AppServicePlan</span></span>
<span data-ttu-id="05a6b-126">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="05a6b-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="05a6b-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="05a6b-127">-AppSettings</span></span>
<span data-ttu-id="05a6b-128">앱 설정 테이블.</span><span class="sxs-lookup"><span data-stu-id="05a6b-128">App Settings HashTable.</span></span> <span data-ttu-id="05a6b-129">기존 앱 설정이 바뀌고 제공 되지 않은 설정은 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="05a6b-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05a6b-130">-AsJob</span></span>
<span data-ttu-id="05a6b-131">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="05a6b-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05a6b-132">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="05a6b-132">-AssignIdentity</span></span>
<span data-ttu-id="05a6b-133">기존 azure web app 또는 functionapp에서 MSI 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="05a6b-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="05a6b-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="05a6b-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="05a6b-135">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="05a6b-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="05a6b-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="05a6b-136">-AzureStoragePath</span></span>
<span data-ttu-id="05a6b-137">컨테이너에 대 한 웹 앱 내에 탑재 하는 Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="05a6b-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="05a6b-138">New-AzureRmWebAppAzureStoragePath를 사용 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="05a6b-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="05a6b-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="05a6b-139">-ConnectionStrings</span></span>
<span data-ttu-id="05a6b-140">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="05a6b-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="05a6b-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="05a6b-141">-ContainerImageName</span></span>
<span data-ttu-id="05a6b-142">컨테이너 이미지 이름</span><span class="sxs-lookup"><span data-stu-id="05a6b-142">Container Image Name</span></span>

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

### <span data-ttu-id="05a6b-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="05a6b-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="05a6b-144">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="05a6b-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="05a6b-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="05a6b-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="05a6b-146">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="05a6b-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="05a6b-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="05a6b-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="05a6b-148">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="05a6b-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="05a6b-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="05a6b-149">-DefaultDocuments</span></span>
<span data-ttu-id="05a6b-150">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="05a6b-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="05a6b-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a6b-151">-DefaultProfile</span></span>
<span data-ttu-id="05a6b-152">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05a6b-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="05a6b-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="05a6b-154">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="05a6b-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="05a6b-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="05a6b-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="05a6b-156">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="05a6b-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="05a6b-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="05a6b-157">-FtpsState</span></span>
<span data-ttu-id="05a6b-158">앱에 대 한 Ftps 상태 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="05a6b-159">허용 되는 값 [AllAllowed | 사용할 수 없음 | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="05a6b-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="05a6b-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="05a6b-160">-HandlerMappings</span></span>
<span data-ttu-id="05a6b-161">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="05a6b-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="05a6b-162">-호스트 이름</span><span class="sxs-lookup"><span data-stu-id="05a6b-162">-HostNames</span></span>
<span data-ttu-id="05a6b-163">Web app 호스트 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="05a6b-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="05a6b-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="05a6b-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="05a6b-165">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="05a6b-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="05a6b-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="05a6b-166">-HttpsOnly</span></span>
<span data-ttu-id="05a6b-167">기존 azure web app 또는 functionapp에서 HTTPS로 모든 트래픽 리디렉션 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="05a6b-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="05a6b-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="05a6b-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="05a6b-169">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="05a6b-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="05a6b-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="05a6b-170">-MinTlsVersion</span></span>
<span data-ttu-id="05a6b-171">SSL 요청에 필요한 TLS의 최소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="05a6b-172">허용 되는 값 [1.0 | 1.1 | 1.2].</span><span class="sxs-lookup"><span data-stu-id="05a6b-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="05a6b-173">-이름</span><span class="sxs-lookup"><span data-stu-id="05a6b-173">-Name</span></span>
<span data-ttu-id="05a6b-174">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="05a6b-174">WebApp Name</span></span>

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

### <span data-ttu-id="05a6b-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="05a6b-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="05a6b-176">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="05a6b-176">Net Framework Version</span></span>

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

### <span data-ttu-id="05a6b-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="05a6b-177">-NumberOfWorkers</span></span>
<span data-ttu-id="05a6b-178">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="05a6b-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="05a6b-179">-PhpVersion</span></span>
<span data-ttu-id="05a6b-180">Php 버전</span><span class="sxs-lookup"><span data-stu-id="05a6b-180">Php Version</span></span>

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

### <span data-ttu-id="05a6b-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="05a6b-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="05a6b-182">요청 추적 사용</span><span class="sxs-lookup"><span data-stu-id="05a6b-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="05a6b-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05a6b-183">-ResourceGroupName</span></span>
<span data-ttu-id="05a6b-184">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="05a6b-184">Resource Group Name</span></span>

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

### <span data-ttu-id="05a6b-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="05a6b-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="05a6b-186">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="05a6b-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="05a6b-187">-Web app</span><span class="sxs-lookup"><span data-stu-id="05a6b-187">-WebApp</span></span>
<span data-ttu-id="05a6b-188">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="05a6b-188">WebApp Object</span></span>

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

### <span data-ttu-id="05a6b-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="05a6b-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="05a6b-190">WebSocketsEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="05a6b-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="05a6b-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a6b-191">CommonParameters</span></span>
<span data-ttu-id="05a6b-192">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a6b-193">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="05a6b-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a6b-194">입력</span><span class="sxs-lookup"><span data-stu-id="05a6b-194">INPUTS</span></span>

### <span data-ttu-id="05a6b-195">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="05a6b-195">System.Int32</span></span>

### <span data-ttu-id="05a6b-196">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="05a6b-196">System.String</span></span>

### <span data-ttu-id="05a6b-197">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="05a6b-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="05a6b-198">출력</span><span class="sxs-lookup"><span data-stu-id="05a6b-198">OUTPUTS</span></span>

### <span data-ttu-id="05a6b-199">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="05a6b-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="05a6b-200">상속자</span><span class="sxs-lookup"><span data-stu-id="05a6b-200">NOTES</span></span>
<span data-ttu-id="05a6b-201">제공 된 cmdlet 아래에서 Azure Web App을 **DOTNETCORE** 로 업데이트 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="05a6b-202">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "Default-Web-WestUS"-ResourceType Microsoft. 웹/사이트/config-Context.resourcename "ContosoWebApp/metadata"-ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="05a6b-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="05a6b-203">Default-WestUS의 값을 web app 이름으로 web app 및 ContosoWebApp의 리소스 그룹 이름으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="05a6b-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="05a6b-204">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05a6b-204">RELATED LINKS</span></span>

[<span data-ttu-id="05a6b-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="05a6b-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="05a6b-206">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="05a6b-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="05a6b-207">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="05a6b-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="05a6b-208">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="05a6b-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="05a6b-209">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="05a6b-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="05a6b-210">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="05a6b-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="05a6b-211">새로운 AzResource</span><span class="sxs-lookup"><span data-stu-id="05a6b-211">New-AzResource</span></span>](./New-AzResource.md)
