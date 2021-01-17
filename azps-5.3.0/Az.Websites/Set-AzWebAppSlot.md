---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491407"
---
# <span data-ttu-id="8c29f-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c29f-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="8c29f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c29f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c29f-103">Azure 웹앱 슬롯을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="8c29f-104">구문</span><span class="sxs-lookup"><span data-stu-id="8c29f-104">SYNTAX</span></span>

### <span data-ttu-id="8c29f-105">S1</span><span class="sxs-lookup"><span data-stu-id="8c29f-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-AlwaysOn <Boolean>] [-MinTlsVersion <String>]
 [-FtpsState <String>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c29f-106">S2</span><span class="sxs-lookup"><span data-stu-id="8c29f-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c29f-107">설명</span><span class="sxs-lookup"><span data-stu-id="8c29f-107">DESCRIPTION</span></span>
<span data-ttu-id="8c29f-108">**Set-AzWebApp** cmdlet은 Azure 웹앱 슬롯을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="8c29f-109">예제</span><span class="sxs-lookup"><span data-stu-id="8c29f-109">EXAMPLES</span></span>

### <span data-ttu-id="8c29f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8c29f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="8c29f-111">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 Webapp ContosoWebApp에서 Slot001과 연결된 appservice 계획을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="8c29f-112">이 링크를 사용하여 연결된 AppService 계획 및 제약 조건 변경에 대해 자세히 알아보면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="8c29f-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="8c29f-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="8c29f-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="8c29f-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="8c29f-115">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 웹앱 ContosoWebApp과 관련된 Slot Slot001에 대해 HttpLoggingEnabled를 true로 설정</span><span class="sxs-lookup"><span data-stu-id="8c29f-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="8c29f-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="8c29f-116">Example 3</span></span>

<span data-ttu-id="8c29f-117">Azure 웹앱 슬롯을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="8c29f-118">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="8c29f-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="8c29f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c29f-119">PARAMETERS</span></span>

### <span data-ttu-id="8c29f-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="8c29f-120">-AlwaysOn</span></span>
<span data-ttu-id="8c29f-121">웹앱이 유휴된 후 언로드되지 않고 항상 로드되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="8c29f-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c29f-122">-AppServicePlan</span></span>
<span data-ttu-id="8c29f-123">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="8c29f-123">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="8c29f-124">-AppSettings</span></span>
<span data-ttu-id="8c29f-125">앱 설정 해시테이블.</span><span class="sxs-lookup"><span data-stu-id="8c29f-125">App Settings HashTable.</span></span> <span data-ttu-id="8c29f-126">기존 앱 설정이 대체됩니다. 이 설정은 제공되지 않은 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c29f-127">-AsJob</span></span>
<span data-ttu-id="8c29f-128">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8c29f-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c29f-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8c29f-129">-AssignIdentity</span></span>
<span data-ttu-id="8c29f-130">기존 슬롯에서 MSI 사용/사용 안 하도록 설정 [미리 보기]</span><span class="sxs-lookup"><span data-stu-id="8c29f-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="8c29f-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="8c29f-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="8c29f-132">자동 교환에 대한 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="8c29f-132">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="8c29f-133">-AzureStoragePath</span></span>
<span data-ttu-id="8c29f-134">Web App for Container 내부에 탑재할 Azure Storage입니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="8c29f-135">이 New-AzureRmWebAppAzureStoragePath 사용하여 만들기</span><span class="sxs-lookup"><span data-stu-id="8c29f-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="8c29f-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="8c29f-136">-ConnectionStrings</span></span>
<span data-ttu-id="8c29f-137">연결 문자열 해시Table</span><span class="sxs-lookup"><span data-stu-id="8c29f-137">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="8c29f-138">-ContainerImageName</span></span>
<span data-ttu-id="8c29f-139">컨테이너 이미지 이름</span><span class="sxs-lookup"><span data-stu-id="8c29f-139">Container Image Name</span></span>

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

### <span data-ttu-id="8c29f-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="8c29f-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="8c29f-141">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="8c29f-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="8c29f-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="8c29f-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="8c29f-143">개인 컨테이너 레지스트리 서버 URL</span><span class="sxs-lookup"><span data-stu-id="8c29f-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="8c29f-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="8c29f-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="8c29f-145">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="8c29f-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="8c29f-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="8c29f-146">-DefaultDocuments</span></span>
<span data-ttu-id="8c29f-147">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="8c29f-147">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c29f-148">-DefaultProfile</span></span>
<span data-ttu-id="8c29f-149">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c29f-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8c29f-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="8c29f-151">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="8c29f-151">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="8c29f-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="8c29f-153">컨테이너 연속 배포 웹후크를 활성화/비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="8c29f-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="8c29f-154">-FtpsState</span></span>
<span data-ttu-id="8c29f-155">앱에 대한 Ftps 상태 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="8c29f-156">허용되는 값 [AllAllowed | 사용 안 으로 설정 | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="8c29f-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="8c29f-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="8c29f-157">-HandlerMappings</span></span>
<span data-ttu-id="8c29f-158">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="8c29f-158">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8c29f-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="8c29f-160">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="8c29f-160">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8c29f-161">-HttpsOnly</span></span>
<span data-ttu-id="8c29f-162">기존 슬롯의 HTTPS로 모든 트래픽 리디렉션 사용/사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="8c29f-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="8c29f-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="8c29f-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="8c29f-164">관리되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="8c29f-164">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8c29f-165">-MinTlsVersion</span></span>
<span data-ttu-id="8c29f-166">SSL 요청에 필요한 TLS의 최소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="8c29f-167">허용되는 값 [1.0 | 1.1 | 1.2].</span><span class="sxs-lookup"><span data-stu-id="8c29f-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="8c29f-168">-Name</span><span class="sxs-lookup"><span data-stu-id="8c29f-168">-Name</span></span>
<span data-ttu-id="8c29f-169">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="8c29f-169">WebApp Name</span></span>

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

### <span data-ttu-id="8c29f-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="8c29f-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="8c29f-171">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="8c29f-171">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="8c29f-172">-NumberOfWorkers</span></span>
<span data-ttu-id="8c29f-173">할당할 작업자 수</span><span class="sxs-lookup"><span data-stu-id="8c29f-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="8c29f-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="8c29f-174">-PhpVersion</span></span>
<span data-ttu-id="8c29f-175">Php 버전</span><span class="sxs-lookup"><span data-stu-id="8c29f-175">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="8c29f-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="8c29f-177">요청 추적 사용 부울</span><span class="sxs-lookup"><span data-stu-id="8c29f-177">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c29f-178">-ResourceGroupName</span></span>
<span data-ttu-id="8c29f-179">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8c29f-179">Resource Group Name</span></span>

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

### <span data-ttu-id="8c29f-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="8c29f-180">-Slot</span></span>
<span data-ttu-id="8c29f-181">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="8c29f-181">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="8c29f-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="8c29f-183">32비트 Worker 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="8c29f-183">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c29f-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8c29f-184">-WebApp</span></span>
<span data-ttu-id="8c29f-185">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="8c29f-185">WebApp Object</span></span>

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

### <span data-ttu-id="8c29f-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="8c29f-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="8c29f-187">웹 소켓 사용 부울</span><span class="sxs-lookup"><span data-stu-id="8c29f-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="8c29f-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c29f-188">CommonParameters</span></span>
<span data-ttu-id="8c29f-189">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c29f-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c29f-190">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8c29f-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c29f-191">입력</span><span class="sxs-lookup"><span data-stu-id="8c29f-191">INPUTS</span></span>

### <span data-ttu-id="8c29f-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8c29f-192">System.Int32</span></span>

### <span data-ttu-id="8c29f-193">System.String</span><span class="sxs-lookup"><span data-stu-id="8c29f-193">System.String</span></span>

### <span data-ttu-id="8c29f-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8c29f-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8c29f-195">출력</span><span class="sxs-lookup"><span data-stu-id="8c29f-195">OUTPUTS</span></span>

### <span data-ttu-id="8c29f-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8c29f-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8c29f-197">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8c29f-197">NOTES</span></span>

## <span data-ttu-id="8c29f-198">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c29f-198">RELATED LINKS</span></span>

[<span data-ttu-id="8c29f-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c29f-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8c29f-200">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c29f-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="8c29f-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c29f-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="8c29f-202">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c29f-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="8c29f-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c29f-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="8c29f-204">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c29f-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8c29f-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c29f-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
