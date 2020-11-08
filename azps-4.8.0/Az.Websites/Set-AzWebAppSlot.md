---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214656"
---
# <span data-ttu-id="fea9c-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fea9c-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="fea9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea9c-102">SYNOPSIS</span></span>
<span data-ttu-id="fea9c-103">Azure Web App 슬롯을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="fea9c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fea9c-104">SYNTAX</span></span>

### <span data-ttu-id="fea9c-105">S1</span><span class="sxs-lookup"><span data-stu-id="fea9c-105">S1</span></span>
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

### <span data-ttu-id="fea9c-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="fea9c-106">S2</span></span>
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

## <span data-ttu-id="fea9c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fea9c-107">DESCRIPTION</span></span>
<span data-ttu-id="fea9c-108">**Set-AzWebApp** Cmdlet은 Azure 웹 앱 슬롯을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="fea9c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fea9c-109">EXAMPLES</span></span>

### <span data-ttu-id="fea9c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fea9c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="fea9c-111">이 명령은 Slot001와 연결 된 appservice 요금제를 리소스 그룹 기본값-웹 WestUS와 연결 된 Web app ContosoWebApp으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="fea9c-112">링크를 사용 하 여 appservice 계획 및 관련 제약 조건을 변경 하는 방법에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="fea9c-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="fea9c-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="fea9c-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="fea9c-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="fea9c-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="fea9c-115">이 명령은 리소스 그룹 기본값과 연결 된 웹 앱 ContosoWebApp에 해당 하는 슬롯 Slot001에 대해 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="fea9c-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="fea9c-116">Example 3</span></span>

<span data-ttu-id="fea9c-117">Azure Web App 슬롯을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="fea9c-118">생성</span><span class="sxs-lookup"><span data-stu-id="fea9c-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="fea9c-119">변수</span><span class="sxs-lookup"><span data-stu-id="fea9c-119">PARAMETERS</span></span>

### <span data-ttu-id="fea9c-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="fea9c-120">-AlwaysOn</span></span>
<span data-ttu-id="fea9c-121">웹 앱이 유휴 상태가 된 후에 언로드되기 전에 항상 로드 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="fea9c-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fea9c-122">-AppServicePlan</span></span>
<span data-ttu-id="fea9c-123">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="fea9c-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="fea9c-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="fea9c-124">-AppSettings</span></span>
<span data-ttu-id="fea9c-125">앱 설정 테이블.</span><span class="sxs-lookup"><span data-stu-id="fea9c-125">App Settings HashTable.</span></span> <span data-ttu-id="fea9c-126">기존 앱 설정이 바뀌고 제공 되지 않은 설정은 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="fea9c-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fea9c-127">-AsJob</span></span>
<span data-ttu-id="fea9c-128">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fea9c-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fea9c-129">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="fea9c-129">-AssignIdentity</span></span>
<span data-ttu-id="fea9c-130">기존 슬롯에서 MSI 사용/사용 안 함 [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="fea9c-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="fea9c-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="fea9c-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="fea9c-132">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="fea9c-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="fea9c-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="fea9c-133">-AzureStoragePath</span></span>
<span data-ttu-id="fea9c-134">컨테이너에 대 한 웹 앱 내에 탑재 하는 Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="fea9c-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="fea9c-135">New-AzureRmWebAppAzureStoragePath를 사용 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="fea9c-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="fea9c-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="fea9c-136">-ConnectionStrings</span></span>
<span data-ttu-id="fea9c-137">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="fea9c-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="fea9c-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="fea9c-138">-ContainerImageName</span></span>
<span data-ttu-id="fea9c-139">컨테이너 이미지 이름</span><span class="sxs-lookup"><span data-stu-id="fea9c-139">Container Image Name</span></span>

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

### <span data-ttu-id="fea9c-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="fea9c-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="fea9c-141">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="fea9c-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="fea9c-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="fea9c-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="fea9c-143">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="fea9c-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="fea9c-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="fea9c-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="fea9c-145">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="fea9c-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="fea9c-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="fea9c-146">-DefaultDocuments</span></span>
<span data-ttu-id="fea9c-147">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="fea9c-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="fea9c-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea9c-148">-DefaultProfile</span></span>
<span data-ttu-id="fea9c-149">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fea9c-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="fea9c-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="fea9c-151">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="fea9c-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="fea9c-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="fea9c-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="fea9c-153">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="fea9c-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="fea9c-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="fea9c-154">-FtpsState</span></span>
<span data-ttu-id="fea9c-155">앱에 대 한 Ftps 상태 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="fea9c-156">허용 되는 값 [AllAllowed | 사용할 수 없음 | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="fea9c-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="fea9c-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="fea9c-157">-HandlerMappings</span></span>
<span data-ttu-id="fea9c-158">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="fea9c-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="fea9c-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="fea9c-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="fea9c-160">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="fea9c-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="fea9c-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="fea9c-161">-HttpsOnly</span></span>
<span data-ttu-id="fea9c-162">기존 슬롯에서 모든 트래픽을 HTTPS로 리디렉션하는 기능 설정/해제</span><span class="sxs-lookup"><span data-stu-id="fea9c-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="fea9c-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="fea9c-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="fea9c-164">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="fea9c-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="fea9c-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="fea9c-165">-MinTlsVersion</span></span>
<span data-ttu-id="fea9c-166">SSL 요청에 필요한 TLS의 최소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="fea9c-167">허용 되는 값 [1.0 | 1.1 | 1.2].</span><span class="sxs-lookup"><span data-stu-id="fea9c-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="fea9c-168">-이름</span><span class="sxs-lookup"><span data-stu-id="fea9c-168">-Name</span></span>
<span data-ttu-id="fea9c-169">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="fea9c-169">WebApp Name</span></span>

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

### <span data-ttu-id="fea9c-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="fea9c-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="fea9c-171">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="fea9c-171">Net Framework Version</span></span>

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

### <span data-ttu-id="fea9c-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="fea9c-172">-NumberOfWorkers</span></span>
<span data-ttu-id="fea9c-173">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="fea9c-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="fea9c-174">-PhpVersion</span></span>
<span data-ttu-id="fea9c-175">Php 버전</span><span class="sxs-lookup"><span data-stu-id="fea9c-175">Php Version</span></span>

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

### <span data-ttu-id="fea9c-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="fea9c-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="fea9c-177">추적을 사용 하 여 부울 요청</span><span class="sxs-lookup"><span data-stu-id="fea9c-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="fea9c-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea9c-178">-ResourceGroupName</span></span>
<span data-ttu-id="fea9c-179">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fea9c-179">Resource Group Name</span></span>

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

### <span data-ttu-id="fea9c-180">-슬롯</span><span class="sxs-lookup"><span data-stu-id="fea9c-180">-Slot</span></span>
<span data-ttu-id="fea9c-181">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="fea9c-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="fea9c-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="fea9c-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="fea9c-183">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="fea9c-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="fea9c-184">-Web app</span><span class="sxs-lookup"><span data-stu-id="fea9c-184">-WebApp</span></span>
<span data-ttu-id="fea9c-185">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="fea9c-185">WebApp Object</span></span>

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

### <span data-ttu-id="fea9c-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="fea9c-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="fea9c-187">웹 소켓 사용 부울</span><span class="sxs-lookup"><span data-stu-id="fea9c-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="fea9c-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea9c-188">CommonParameters</span></span>
<span data-ttu-id="fea9c-189">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fea9c-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea9c-190">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fea9c-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea9c-191">입력</span><span class="sxs-lookup"><span data-stu-id="fea9c-191">INPUTS</span></span>

### <span data-ttu-id="fea9c-192">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="fea9c-192">System.Int32</span></span>

### <span data-ttu-id="fea9c-193">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fea9c-193">System.String</span></span>

### <span data-ttu-id="fea9c-194">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="fea9c-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fea9c-195">출력</span><span class="sxs-lookup"><span data-stu-id="fea9c-195">OUTPUTS</span></span>

### <span data-ttu-id="fea9c-196">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="fea9c-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fea9c-197">상속자</span><span class="sxs-lookup"><span data-stu-id="fea9c-197">NOTES</span></span>

## <span data-ttu-id="fea9c-198">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fea9c-198">RELATED LINKS</span></span>

[<span data-ttu-id="fea9c-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fea9c-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="fea9c-200">새로운 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fea9c-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="fea9c-201">제거-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fea9c-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="fea9c-202">다시 시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fea9c-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="fea9c-203">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fea9c-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="fea9c-204">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fea9c-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="fea9c-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fea9c-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
