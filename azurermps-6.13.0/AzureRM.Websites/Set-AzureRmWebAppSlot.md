---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4ba94f0f7633feefc32c0b32d820e8bee9b6d1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530809"
---
# <span data-ttu-id="8c459-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c459-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="8c459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c459-102">SYNOPSIS</span></span>
<span data-ttu-id="8c459-103">Azure Web App 슬롯을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c459-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c459-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8c459-104">SYNTAX</span></span>

### <span data-ttu-id="8c459-105">S1</span><span class="sxs-lookup"><span data-stu-id="8c459-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c459-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="8c459-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c459-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8c459-107">DESCRIPTION</span></span>
<span data-ttu-id="8c459-108">**Set-AzureRmWebApp** Cmdlet은 Azure 웹 앱 슬롯을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c459-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="8c459-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8c459-109">EXAMPLES</span></span>

### <span data-ttu-id="8c459-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8c459-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="8c459-111">이 명령은 리소스 그룹 기본값과 연결 된 웹 앱 ContosoWebApp에 해당 하는 슬롯 Slot001에 대해 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c459-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="8c459-112">변수</span><span class="sxs-lookup"><span data-stu-id="8c459-112">PARAMETERS</span></span>

### <span data-ttu-id="8c459-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c459-113">-AppServicePlan</span></span>
<span data-ttu-id="8c459-114">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="8c459-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="8c459-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="8c459-115">-AppSettings</span></span>
<span data-ttu-id="8c459-116">앱 설정 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="8c459-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="8c459-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c459-117">-AsJob</span></span>
<span data-ttu-id="8c459-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8c459-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c459-119">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="8c459-119">-AssignIdentity</span></span>
<span data-ttu-id="8c459-120">기존 슬롯에서 MSI 사용/사용 안 함 [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="8c459-120">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="8c459-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="8c459-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="8c459-122">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="8c459-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="8c459-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="8c459-123">-ConnectionStrings</span></span>
<span data-ttu-id="8c459-124">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="8c459-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="8c459-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="8c459-125">-ContainerImageName</span></span>
<span data-ttu-id="8c459-126">컨테이너 이미지 이름</span><span class="sxs-lookup"><span data-stu-id="8c459-126">Container Image Name</span></span>

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

### <span data-ttu-id="8c459-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="8c459-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="8c459-128">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="8c459-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="8c459-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="8c459-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="8c459-130">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="8c459-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="8c459-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="8c459-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="8c459-132">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="8c459-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="8c459-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="8c459-133">-DefaultDocuments</span></span>
<span data-ttu-id="8c459-134">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="8c459-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="8c459-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c459-135">-DefaultProfile</span></span>
<span data-ttu-id="8c459-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c459-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c459-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8c459-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="8c459-138">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="8c459-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="8c459-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="8c459-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="8c459-140">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="8c459-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="8c459-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="8c459-141">-HandlerMappings</span></span>
<span data-ttu-id="8c459-142">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="8c459-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="8c459-143">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="8c459-143">-HttpLoggingEnabled</span></span>
<span data-ttu-id="8c459-144">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="8c459-144">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="8c459-145">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8c459-145">-HttpsOnly</span></span>
<span data-ttu-id="8c459-146">기존 슬롯에서 모든 트래픽을 HTTPS로 리디렉션하는 기능 설정/해제</span><span class="sxs-lookup"><span data-stu-id="8c459-146">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="8c459-147">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="8c459-147">-ManagedPipelineMode</span></span>
<span data-ttu-id="8c459-148">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="8c459-148">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="8c459-149">-이름</span><span class="sxs-lookup"><span data-stu-id="8c459-149">-Name</span></span>
<span data-ttu-id="8c459-150">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="8c459-150">WebApp Name</span></span>

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

### <span data-ttu-id="8c459-151">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="8c459-151">-NetFrameworkVersion</span></span>
<span data-ttu-id="8c459-152">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="8c459-152">Net Framework Version</span></span>

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

### <span data-ttu-id="8c459-153">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="8c459-153">-NumberOfWorkers</span></span>
<span data-ttu-id="8c459-154">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8c459-154">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="8c459-155">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="8c459-155">-PhpVersion</span></span>
<span data-ttu-id="8c459-156">Php 버전</span><span class="sxs-lookup"><span data-stu-id="8c459-156">Php Version</span></span>

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

### <span data-ttu-id="8c459-157">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="8c459-157">-RequestTracingEnabled</span></span>
<span data-ttu-id="8c459-158">추적을 사용 하 여 부울 요청</span><span class="sxs-lookup"><span data-stu-id="8c459-158">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="8c459-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c459-159">-ResourceGroupName</span></span>
<span data-ttu-id="8c459-160">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8c459-160">Resource Group Name</span></span>

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

### <span data-ttu-id="8c459-161">-슬롯</span><span class="sxs-lookup"><span data-stu-id="8c459-161">-Slot</span></span>
<span data-ttu-id="8c459-162">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="8c459-162">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8c459-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="8c459-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="8c459-164">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="8c459-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="8c459-165">-Web app</span><span class="sxs-lookup"><span data-stu-id="8c459-165">-WebApp</span></span>
<span data-ttu-id="8c459-166">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="8c459-166">WebApp Object</span></span>

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

### <span data-ttu-id="8c459-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="8c459-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="8c459-168">웹 소켓 사용 부울</span><span class="sxs-lookup"><span data-stu-id="8c459-168">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="8c459-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c459-169">CommonParameters</span></span>
<span data-ttu-id="8c459-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c459-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c459-171">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c459-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c459-172">입력</span><span class="sxs-lookup"><span data-stu-id="8c459-172">INPUTS</span></span>

### <span data-ttu-id="8c459-173">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="8c459-173">System.Int32</span></span>
<span data-ttu-id="8c459-174">매개 변수: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8c459-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="8c459-175">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8c459-175">System.String</span></span>

### <span data-ttu-id="8c459-176">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="8c459-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="8c459-177">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8c459-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="8c459-178">출력</span><span class="sxs-lookup"><span data-stu-id="8c459-178">OUTPUTS</span></span>

### <span data-ttu-id="8c459-179">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="8c459-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="8c459-180">상속자</span><span class="sxs-lookup"><span data-stu-id="8c459-180">NOTES</span></span>

## <span data-ttu-id="8c459-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c459-181">RELATED LINKS</span></span>

[<span data-ttu-id="8c459-182">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c459-182">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="8c459-183">새로운 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c459-183">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="8c459-184">제거-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c459-184">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="8c459-185">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c459-185">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="8c459-186">시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c459-186">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="8c459-187">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c459-187">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="8c459-188">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c459-188">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
