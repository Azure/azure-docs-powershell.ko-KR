---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d0bca8fadf9179990eb5901e67ee07a3532a39cb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698293"
---
# <span data-ttu-id="bf005-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf005-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="bf005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf005-102">SYNOPSIS</span></span>
<span data-ttu-id="bf005-103">Azure Web App 슬롯을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf005-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="bf005-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf005-104">SYNTAX</span></span>

### <span data-ttu-id="bf005-105">S1</span><span class="sxs-lookup"><span data-stu-id="bf005-105">S1</span></span>
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
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf005-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="bf005-106">S2</span></span>
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

## <span data-ttu-id="bf005-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bf005-107">DESCRIPTION</span></span>
<span data-ttu-id="bf005-108">**Set-AzWebApp** Cmdlet은 Azure 웹 앱 슬롯을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf005-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="bf005-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bf005-109">EXAMPLES</span></span>

### <span data-ttu-id="bf005-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf005-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="bf005-111">이 명령은 Slot001와 연결 된 appservice 요금제를 리소스 그룹 기본값-웹 WestUS와 연결 된 Web app ContosoWebApp으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf005-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="bf005-112">링크를 사용 하 여 관련 된 appservice 계획 및 제약 조건을 변경 하는 방법에 대 한 자세한 learm.</span><span class="sxs-lookup"><span data-stu-id="bf005-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="bf005-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="bf005-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="bf005-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="bf005-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="bf005-115">이 명령은 리소스 그룹 기본값과 연결 된 웹 앱 ContosoWebApp에 해당 하는 슬롯 Slot001에 대해 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf005-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="bf005-116">변수</span><span class="sxs-lookup"><span data-stu-id="bf005-116">PARAMETERS</span></span>

### <span data-ttu-id="bf005-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bf005-117">-AppServicePlan</span></span>
<span data-ttu-id="bf005-118">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="bf005-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="bf005-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="bf005-119">-AppSettings</span></span>
<span data-ttu-id="bf005-120">앱 설정 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="bf005-120">App Settings HashTable</span></span>

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

### <span data-ttu-id="bf005-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf005-121">-AsJob</span></span>
<span data-ttu-id="bf005-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bf005-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf005-123">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="bf005-123">-AssignIdentity</span></span>
<span data-ttu-id="bf005-124">기존 슬롯에서 MSI 사용/사용 안 함 [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="bf005-124">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="bf005-125">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="bf005-125">-AutoSwapSlotName</span></span>
<span data-ttu-id="bf005-126">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="bf005-126">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="bf005-127">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="bf005-127">-AzureStoragePath</span></span>
<span data-ttu-id="bf005-128">컨테이너에 대 한 웹 앱 내에 탑재 하는 Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bf005-128">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="bf005-129">New-AzureRmWebAppAzureStoragePath를 사용 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="bf005-129">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="bf005-130">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="bf005-130">-ConnectionStrings</span></span>
<span data-ttu-id="bf005-131">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="bf005-131">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="bf005-132">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="bf005-132">-ContainerImageName</span></span>
<span data-ttu-id="bf005-133">컨테이너 이미지 이름</span><span class="sxs-lookup"><span data-stu-id="bf005-133">Container Image Name</span></span>

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

### <span data-ttu-id="bf005-134">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="bf005-134">-ContainerRegistryPassword</span></span>
<span data-ttu-id="bf005-135">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="bf005-135">Private Container Registry Password</span></span>

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

### <span data-ttu-id="bf005-136">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="bf005-136">-ContainerRegistryUrl</span></span>
<span data-ttu-id="bf005-137">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="bf005-137">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="bf005-138">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="bf005-138">-ContainerRegistryUser</span></span>
<span data-ttu-id="bf005-139">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="bf005-139">Private Container Registry Username</span></span>

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

### <span data-ttu-id="bf005-140">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="bf005-140">-DefaultDocuments</span></span>
<span data-ttu-id="bf005-141">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="bf005-141">Default Documents String Array</span></span>

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

### <span data-ttu-id="bf005-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf005-142">-DefaultProfile</span></span>
<span data-ttu-id="bf005-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf005-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf005-144">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="bf005-144">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="bf005-145">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="bf005-145">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="bf005-146">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="bf005-146">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="bf005-147">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="bf005-147">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="bf005-148">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="bf005-148">-HandlerMappings</span></span>
<span data-ttu-id="bf005-149">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="bf005-149">Handler Mappings IList</span></span>

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

### <span data-ttu-id="bf005-150">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="bf005-150">-HttpLoggingEnabled</span></span>
<span data-ttu-id="bf005-151">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="bf005-151">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="bf005-152">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="bf005-152">-HttpsOnly</span></span>
<span data-ttu-id="bf005-153">기존 슬롯에서 모든 트래픽을 HTTPS로 리디렉션하는 기능 설정/해제</span><span class="sxs-lookup"><span data-stu-id="bf005-153">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="bf005-154">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="bf005-154">-ManagedPipelineMode</span></span>
<span data-ttu-id="bf005-155">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="bf005-155">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="bf005-156">-이름</span><span class="sxs-lookup"><span data-stu-id="bf005-156">-Name</span></span>
<span data-ttu-id="bf005-157">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="bf005-157">WebApp Name</span></span>

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

### <span data-ttu-id="bf005-158">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="bf005-158">-NetFrameworkVersion</span></span>
<span data-ttu-id="bf005-159">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="bf005-159">Net Framework Version</span></span>

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

### <span data-ttu-id="bf005-160">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="bf005-160">-NumberOfWorkers</span></span>
<span data-ttu-id="bf005-161">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bf005-161">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="bf005-162">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="bf005-162">-PhpVersion</span></span>
<span data-ttu-id="bf005-163">Php 버전</span><span class="sxs-lookup"><span data-stu-id="bf005-163">Php Version</span></span>

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

### <span data-ttu-id="bf005-164">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="bf005-164">-RequestTracingEnabled</span></span>
<span data-ttu-id="bf005-165">추적을 사용 하 여 부울 요청</span><span class="sxs-lookup"><span data-stu-id="bf005-165">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="bf005-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf005-166">-ResourceGroupName</span></span>
<span data-ttu-id="bf005-167">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bf005-167">Resource Group Name</span></span>

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

### <span data-ttu-id="bf005-168">-슬롯</span><span class="sxs-lookup"><span data-stu-id="bf005-168">-Slot</span></span>
<span data-ttu-id="bf005-169">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="bf005-169">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bf005-170">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="bf005-170">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="bf005-171">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="bf005-171">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="bf005-172">-Web app</span><span class="sxs-lookup"><span data-stu-id="bf005-172">-WebApp</span></span>
<span data-ttu-id="bf005-173">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="bf005-173">WebApp Object</span></span>

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

### <span data-ttu-id="bf005-174">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="bf005-174">-WebSocketsEnabled</span></span>
<span data-ttu-id="bf005-175">웹 소켓 사용 부울</span><span class="sxs-lookup"><span data-stu-id="bf005-175">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="bf005-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf005-176">CommonParameters</span></span>
<span data-ttu-id="bf005-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf005-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf005-178">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf005-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf005-179">입력</span><span class="sxs-lookup"><span data-stu-id="bf005-179">INPUTS</span></span>

### <span data-ttu-id="bf005-180">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="bf005-180">System.Int32</span></span>

### <span data-ttu-id="bf005-181">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf005-181">System.String</span></span>

### <span data-ttu-id="bf005-182">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="bf005-182">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bf005-183">출력</span><span class="sxs-lookup"><span data-stu-id="bf005-183">OUTPUTS</span></span>

### <span data-ttu-id="bf005-184">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="bf005-184">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bf005-185">상속자</span><span class="sxs-lookup"><span data-stu-id="bf005-185">NOTES</span></span>

## <span data-ttu-id="bf005-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf005-186">RELATED LINKS</span></span>

[<span data-ttu-id="bf005-187">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf005-187">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="bf005-188">새로운 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf005-188">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="bf005-189">제거-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf005-189">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="bf005-190">다시 시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf005-190">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="bf005-191">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf005-191">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="bf005-192">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf005-192">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="bf005-193">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bf005-193">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
