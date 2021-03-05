---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d07d85aa9747982f223d45c40fc8897a0b0e3e73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011104"
---
# <span data-ttu-id="f03dd-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f03dd-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="f03dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f03dd-102">SYNOPSIS</span></span>
<span data-ttu-id="f03dd-103">Azure Web App 슬롯을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="f03dd-104">구문</span><span class="sxs-lookup"><span data-stu-id="f03dd-104">SYNTAX</span></span>

### <span data-ttu-id="f03dd-105">S1</span><span class="sxs-lookup"><span data-stu-id="f03dd-105">S1</span></span>
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

### <span data-ttu-id="f03dd-106">S2</span><span class="sxs-lookup"><span data-stu-id="f03dd-106">S2</span></span>
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

## <span data-ttu-id="f03dd-107">설명</span><span class="sxs-lookup"><span data-stu-id="f03dd-107">DESCRIPTION</span></span>
<span data-ttu-id="f03dd-108">**Set-AzWebApp** cmdlet은 Azure Web App Slot을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="f03dd-109">예제</span><span class="sxs-lookup"><span data-stu-id="f03dd-109">EXAMPLES</span></span>

### <span data-ttu-id="f03dd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f03dd-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="f03dd-111">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 Webapp ContosoWebApp에서 Slot001과 연결된 appservice 계획을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="f03dd-112">이 링크를 사용하여 연결된 appservice 계획 및 제약 조건을 변경하는 방법을 자세히 알아보면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="f03dd-113"> https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="f03dd-113">https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="f03dd-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f03dd-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="f03dd-115">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 Web App ContosoWebApp과 관련된 Slot Slot001에 대해 httpLoggingEnabled를 true로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="f03dd-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="f03dd-116">Example 3</span></span>

<span data-ttu-id="f03dd-117">Azure Web App 슬롯을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="f03dd-118">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="f03dd-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="f03dd-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f03dd-119">PARAMETERS</span></span>

### <span data-ttu-id="f03dd-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="f03dd-120">-AlwaysOn</span></span>
<span data-ttu-id="f03dd-121">웹앱이 유휴 후에 로드되지 않고 항상 로드되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="f03dd-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f03dd-122">-AppServicePlan</span></span>
<span data-ttu-id="f03dd-123">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="f03dd-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="f03dd-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="f03dd-124">-AppSettings</span></span>
<span data-ttu-id="f03dd-125">앱 설정 해시테이블</span><span class="sxs-lookup"><span data-stu-id="f03dd-125">App Settings HashTable.</span></span> <span data-ttu-id="f03dd-126">기존 앱 설정이 대체됩니다. 제공되지 않은 모든 설정이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="f03dd-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f03dd-127">-AsJob</span></span>
<span data-ttu-id="f03dd-128">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f03dd-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f03dd-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f03dd-129">-AssignIdentity</span></span>
<span data-ttu-id="f03dd-130">기존 슬롯에서 MSI 사용/사용 안 하도록 설정 [미리 보기]</span><span class="sxs-lookup"><span data-stu-id="f03dd-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="f03dd-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="f03dd-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="f03dd-132">자동 교환의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="f03dd-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="f03dd-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="f03dd-133">-AzureStoragePath</span></span>
<span data-ttu-id="f03dd-134">Azure Storage를 사용하여 컨테이너용 웹앱 내부에 탑재합니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="f03dd-135">New-AzureRmWebAppAzureStoragePath 사용하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="f03dd-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="f03dd-136">-ConnectionStrings</span></span>
<span data-ttu-id="f03dd-137">연결 문자열 해시테이블</span><span class="sxs-lookup"><span data-stu-id="f03dd-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="f03dd-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="f03dd-138">-ContainerImageName</span></span>
<span data-ttu-id="f03dd-139">컨테이너 이미지 이름</span><span class="sxs-lookup"><span data-stu-id="f03dd-139">Container Image Name</span></span>

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

### <span data-ttu-id="f03dd-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="f03dd-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="f03dd-141">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="f03dd-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="f03dd-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="f03dd-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="f03dd-143">개인 컨테이너 레지스트리 서버 URL</span><span class="sxs-lookup"><span data-stu-id="f03dd-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="f03dd-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="f03dd-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="f03dd-145">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="f03dd-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="f03dd-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="f03dd-146">-DefaultDocuments</span></span>
<span data-ttu-id="f03dd-147">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="f03dd-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="f03dd-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03dd-148">-DefaultProfile</span></span>
<span data-ttu-id="f03dd-149">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f03dd-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="f03dd-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="f03dd-151">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="f03dd-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="f03dd-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="f03dd-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="f03dd-153">컨테이너 연속 배포 웹후크 사용/사용 안 하세요.</span><span class="sxs-lookup"><span data-stu-id="f03dd-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="f03dd-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="f03dd-154">-FtpsState</span></span>
<span data-ttu-id="f03dd-155">앱에 대한 Ftps 상태 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="f03dd-156">허용된 값 [AllAllowed | 비활성화된 | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="f03dd-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="f03dd-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="f03dd-157">-HandlerMappings</span></span>
<span data-ttu-id="f03dd-158">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="f03dd-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="f03dd-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="f03dd-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="f03dd-160">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="f03dd-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="f03dd-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f03dd-161">-HttpsOnly</span></span>
<span data-ttu-id="f03dd-162">기존 슬롯에서 HTTPS로 모든 트래픽 리디렉션을 사용하도록 설정/사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="f03dd-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="f03dd-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="f03dd-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="f03dd-164">관리되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="f03dd-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="f03dd-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f03dd-165">-MinTlsVersion</span></span>
<span data-ttu-id="f03dd-166">SSL 요청에 필요한 최소 버전의 TLS입니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="f03dd-167">허용된 값 [1.0 | 1.1 | 1.2].</span><span class="sxs-lookup"><span data-stu-id="f03dd-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="f03dd-168">-Name</span><span class="sxs-lookup"><span data-stu-id="f03dd-168">-Name</span></span>
<span data-ttu-id="f03dd-169">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="f03dd-169">WebApp Name</span></span>

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

### <span data-ttu-id="f03dd-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="f03dd-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="f03dd-171">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="f03dd-171">Net Framework Version</span></span>

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

### <span data-ttu-id="f03dd-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="f03dd-172">-NumberOfWorkers</span></span>
<span data-ttu-id="f03dd-173">할당할 작업자 수</span><span class="sxs-lookup"><span data-stu-id="f03dd-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="f03dd-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="f03dd-174">-PhpVersion</span></span>
<span data-ttu-id="f03dd-175">Php 버전</span><span class="sxs-lookup"><span data-stu-id="f03dd-175">Php Version</span></span>

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

### <span data-ttu-id="f03dd-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="f03dd-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="f03dd-177">요청 추적 사용 부울</span><span class="sxs-lookup"><span data-stu-id="f03dd-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="f03dd-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f03dd-178">-ResourceGroupName</span></span>
<span data-ttu-id="f03dd-179">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f03dd-179">Resource Group Name</span></span>

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

### <span data-ttu-id="f03dd-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="f03dd-180">-Slot</span></span>
<span data-ttu-id="f03dd-181">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="f03dd-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f03dd-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="f03dd-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="f03dd-183">32비트 Worker 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="f03dd-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="f03dd-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f03dd-184">-WebApp</span></span>
<span data-ttu-id="f03dd-185">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="f03dd-185">WebApp Object</span></span>

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

### <span data-ttu-id="f03dd-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="f03dd-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="f03dd-187">웹 소켓 사용 부울</span><span class="sxs-lookup"><span data-stu-id="f03dd-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="f03dd-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03dd-188">CommonParameters</span></span>
<span data-ttu-id="f03dd-189">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f03dd-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03dd-190">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f03dd-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03dd-191">입력</span><span class="sxs-lookup"><span data-stu-id="f03dd-191">INPUTS</span></span>

### <span data-ttu-id="f03dd-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f03dd-192">System.Int32</span></span>

### <span data-ttu-id="f03dd-193">System.String</span><span class="sxs-lookup"><span data-stu-id="f03dd-193">System.String</span></span>

### <span data-ttu-id="f03dd-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f03dd-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f03dd-195">출력</span><span class="sxs-lookup"><span data-stu-id="f03dd-195">OUTPUTS</span></span>

### <span data-ttu-id="f03dd-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f03dd-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f03dd-197">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f03dd-197">NOTES</span></span>

## <span data-ttu-id="f03dd-198">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f03dd-198">RELATED LINKS</span></span>

[<span data-ttu-id="f03dd-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f03dd-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="f03dd-200">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f03dd-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="f03dd-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f03dd-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="f03dd-202">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f03dd-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="f03dd-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f03dd-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="f03dd-204">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f03dd-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="f03dd-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f03dd-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
