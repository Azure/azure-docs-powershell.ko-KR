---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: ed1e073757eb2fc1b63a6ffd799c55ad1ffaf748
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042601"
---
# <span data-ttu-id="47fc8-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47fc8-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="47fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="47fc8-103">Azure Web App 슬롯을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47fc8-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="47fc8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47fc8-104">SYNTAX</span></span>

### <span data-ttu-id="47fc8-105">S1</span><span class="sxs-lookup"><span data-stu-id="47fc8-105">S1</span></span>
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

### <span data-ttu-id="47fc8-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="47fc8-106">S2</span></span>
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

## <span data-ttu-id="47fc8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="47fc8-107">DESCRIPTION</span></span>
<span data-ttu-id="47fc8-108">**Set-AzWebApp** Cmdlet은 Azure 웹 앱 슬롯을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47fc8-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="47fc8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="47fc8-109">EXAMPLES</span></span>

### <span data-ttu-id="47fc8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="47fc8-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="47fc8-111">이 명령은 Slot001와 연결 된 appservice 요금제를 리소스 그룹 기본값-웹 WestUS와 연결 된 Web app ContosoWebApp으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="47fc8-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="47fc8-112">링크를 사용 하 여 appservice 계획 및 관련 제약 조건을 변경 하는 방법에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="47fc8-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="47fc8-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="47fc8-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="47fc8-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="47fc8-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="47fc8-115">이 명령은 리소스 그룹 기본값과 연결 된 웹 앱 ContosoWebApp에 해당 하는 슬롯 Slot001에 대해 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47fc8-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="47fc8-116">변수</span><span class="sxs-lookup"><span data-stu-id="47fc8-116">PARAMETERS</span></span>

### <span data-ttu-id="47fc8-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="47fc8-117">-AlwaysOn</span></span>
<span data-ttu-id="47fc8-118">웹 앱이 유휴 상태가 된 후에 언로드되기 전에 항상 로드 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="47fc8-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="47fc8-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="47fc8-119">-AppServicePlan</span></span>
<span data-ttu-id="47fc8-120">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="47fc8-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="47fc8-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="47fc8-121">-AppSettings</span></span>
<span data-ttu-id="47fc8-122">앱 설정 테이블.</span><span class="sxs-lookup"><span data-stu-id="47fc8-122">App Settings HashTable.</span></span> <span data-ttu-id="47fc8-123">기존 앱 설정이 바뀌고 제공 되지 않은 설정은 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47fc8-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="47fc8-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47fc8-124">-AsJob</span></span>
<span data-ttu-id="47fc8-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="47fc8-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47fc8-126">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="47fc8-126">-AssignIdentity</span></span>
<span data-ttu-id="47fc8-127">기존 슬롯에서 MSI 사용/사용 안 함 [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="47fc8-127">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="47fc8-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="47fc8-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="47fc8-129">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="47fc8-129">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="47fc8-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="47fc8-130">-AzureStoragePath</span></span>
<span data-ttu-id="47fc8-131">컨테이너에 대 한 웹 앱 내에 탑재 하는 Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="47fc8-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="47fc8-132">New-AzureRmWebAppAzureStoragePath를 사용 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="47fc8-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="47fc8-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="47fc8-133">-ConnectionStrings</span></span>
<span data-ttu-id="47fc8-134">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="47fc8-134">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="47fc8-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="47fc8-135">-ContainerImageName</span></span>
<span data-ttu-id="47fc8-136">컨테이너 이미지 이름</span><span class="sxs-lookup"><span data-stu-id="47fc8-136">Container Image Name</span></span>

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

### <span data-ttu-id="47fc8-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="47fc8-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="47fc8-138">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="47fc8-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="47fc8-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="47fc8-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="47fc8-140">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="47fc8-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="47fc8-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="47fc8-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="47fc8-142">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="47fc8-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="47fc8-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="47fc8-143">-DefaultDocuments</span></span>
<span data-ttu-id="47fc8-144">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="47fc8-144">Default Documents String Array</span></span>

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

### <span data-ttu-id="47fc8-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47fc8-145">-DefaultProfile</span></span>
<span data-ttu-id="47fc8-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47fc8-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47fc8-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="47fc8-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="47fc8-148">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="47fc8-148">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="47fc8-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="47fc8-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="47fc8-150">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="47fc8-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="47fc8-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="47fc8-151">-FtpsState</span></span>
<span data-ttu-id="47fc8-152">앱에 대 한 Ftps 상태 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47fc8-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="47fc8-153">허용 되는 값 [AllAllowed | 사용할 수 없음 | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="47fc8-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="47fc8-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="47fc8-154">-HandlerMappings</span></span>
<span data-ttu-id="47fc8-155">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="47fc8-155">Handler Mappings IList</span></span>

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

### <span data-ttu-id="47fc8-156">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="47fc8-156">-HttpLoggingEnabled</span></span>
<span data-ttu-id="47fc8-157">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="47fc8-157">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="47fc8-158">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="47fc8-158">-HttpsOnly</span></span>
<span data-ttu-id="47fc8-159">기존 슬롯에서 모든 트래픽을 HTTPS로 리디렉션하는 기능 설정/해제</span><span class="sxs-lookup"><span data-stu-id="47fc8-159">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="47fc8-160">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="47fc8-160">-ManagedPipelineMode</span></span>
<span data-ttu-id="47fc8-161">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="47fc8-161">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="47fc8-162">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="47fc8-162">-MinTlsVersion</span></span>
<span data-ttu-id="47fc8-163">SSL 요청에 필요한 TLS의 최소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="47fc8-163">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="47fc8-164">허용 되는 값 [1.0 | 1.1 | 1.2].</span><span class="sxs-lookup"><span data-stu-id="47fc8-164">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="47fc8-165">-이름</span><span class="sxs-lookup"><span data-stu-id="47fc8-165">-Name</span></span>
<span data-ttu-id="47fc8-166">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="47fc8-166">WebApp Name</span></span>

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

### <span data-ttu-id="47fc8-167">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="47fc8-167">-NetFrameworkVersion</span></span>
<span data-ttu-id="47fc8-168">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="47fc8-168">Net Framework Version</span></span>

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

### <span data-ttu-id="47fc8-169">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="47fc8-169">-NumberOfWorkers</span></span>
<span data-ttu-id="47fc8-170">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="47fc8-170">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="47fc8-171">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="47fc8-171">-PhpVersion</span></span>
<span data-ttu-id="47fc8-172">Php 버전</span><span class="sxs-lookup"><span data-stu-id="47fc8-172">Php Version</span></span>

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

### <span data-ttu-id="47fc8-173">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="47fc8-173">-RequestTracingEnabled</span></span>
<span data-ttu-id="47fc8-174">추적을 사용 하 여 부울 요청</span><span class="sxs-lookup"><span data-stu-id="47fc8-174">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="47fc8-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47fc8-175">-ResourceGroupName</span></span>
<span data-ttu-id="47fc8-176">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="47fc8-176">Resource Group Name</span></span>

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

### <span data-ttu-id="47fc8-177">-슬롯</span><span class="sxs-lookup"><span data-stu-id="47fc8-177">-Slot</span></span>
<span data-ttu-id="47fc8-178">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="47fc8-178">WebApp Slot Name</span></span>

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

### <span data-ttu-id="47fc8-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="47fc8-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="47fc8-180">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="47fc8-180">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="47fc8-181">-Web app</span><span class="sxs-lookup"><span data-stu-id="47fc8-181">-WebApp</span></span>
<span data-ttu-id="47fc8-182">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="47fc8-182">WebApp Object</span></span>

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

### <span data-ttu-id="47fc8-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="47fc8-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="47fc8-184">웹 소켓 사용 부울</span><span class="sxs-lookup"><span data-stu-id="47fc8-184">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="47fc8-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47fc8-185">CommonParameters</span></span>
<span data-ttu-id="47fc8-186">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47fc8-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47fc8-187">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="47fc8-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47fc8-188">입력</span><span class="sxs-lookup"><span data-stu-id="47fc8-188">INPUTS</span></span>

### <span data-ttu-id="47fc8-189">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="47fc8-189">System.Int32</span></span>

### <span data-ttu-id="47fc8-190">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="47fc8-190">System.String</span></span>

### <span data-ttu-id="47fc8-191">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="47fc8-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="47fc8-192">출력</span><span class="sxs-lookup"><span data-stu-id="47fc8-192">OUTPUTS</span></span>

### <span data-ttu-id="47fc8-193">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="47fc8-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="47fc8-194">상속자</span><span class="sxs-lookup"><span data-stu-id="47fc8-194">NOTES</span></span>

## <span data-ttu-id="47fc8-195">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47fc8-195">RELATED LINKS</span></span>

[<span data-ttu-id="47fc8-196">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47fc8-196">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="47fc8-197">새로운 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47fc8-197">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="47fc8-198">제거-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47fc8-198">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="47fc8-199">다시 시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47fc8-199">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="47fc8-200">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47fc8-200">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="47fc8-201">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47fc8-201">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="47fc8-202">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="47fc8-202">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
