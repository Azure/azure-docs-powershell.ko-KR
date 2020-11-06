---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: a47f490ae77fc540f3e14708b19dade5ce4e7c3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530025"
---
# <span data-ttu-id="f2335-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2335-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="f2335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2335-102">SYNOPSIS</span></span>
<span data-ttu-id="f2335-103">Azure Web App을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2335-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2335-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2335-104">SYNTAX</span></span>

### <span data-ttu-id="f2335-105">S1</span><span class="sxs-lookup"><span data-stu-id="f2335-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2335-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="f2335-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2335-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f2335-107">DESCRIPTION</span></span>
<span data-ttu-id="f2335-108">**AzureRmWebApp** Cmdlet은 Azure 웹 앱을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2335-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="f2335-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f2335-109">EXAMPLES</span></span>

### <span data-ttu-id="f2335-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2335-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="f2335-111">이 명령은 리소스 그룹 Default-웹에 연결 된 웹 앱 ContosoWebApp에 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2335-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="f2335-112">변수</span><span class="sxs-lookup"><span data-stu-id="f2335-112">PARAMETERS</span></span>

### <span data-ttu-id="f2335-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f2335-113">-AppServicePlan</span></span>
<span data-ttu-id="f2335-114">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="f2335-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="f2335-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="f2335-115">-AppSettings</span></span>
<span data-ttu-id="f2335-116">앱 설정 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="f2335-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="f2335-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2335-117">-AsJob</span></span>
<span data-ttu-id="f2335-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f2335-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2335-119">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="f2335-119">-AssignIdentity</span></span>
<span data-ttu-id="f2335-120">기존 azure web app 또는 functionapp에서 MSI 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="f2335-120">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="f2335-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="f2335-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="f2335-122">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="f2335-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="f2335-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="f2335-123">-ConnectionStrings</span></span>
<span data-ttu-id="f2335-124">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="f2335-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="f2335-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="f2335-125">-ContainerImageName</span></span>
<span data-ttu-id="f2335-126">컨테이너 이미지 이름</span><span class="sxs-lookup"><span data-stu-id="f2335-126">Container Image Name</span></span>

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

### <span data-ttu-id="f2335-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="f2335-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="f2335-128">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="f2335-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="f2335-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="f2335-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="f2335-130">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="f2335-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="f2335-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="f2335-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="f2335-132">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="f2335-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="f2335-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="f2335-133">-DefaultDocuments</span></span>
<span data-ttu-id="f2335-134">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="f2335-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="f2335-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2335-135">-DefaultProfile</span></span>
<span data-ttu-id="f2335-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2335-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2335-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="f2335-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="f2335-138">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="f2335-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="f2335-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="f2335-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="f2335-140">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="f2335-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="f2335-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="f2335-141">-HandlerMappings</span></span>
<span data-ttu-id="f2335-142">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="f2335-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="f2335-143">-호스트 이름</span><span class="sxs-lookup"><span data-stu-id="f2335-143">-HostNames</span></span>
<span data-ttu-id="f2335-144">Web app 호스트 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="f2335-144">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="f2335-145">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="f2335-145">-HttpLoggingEnabled</span></span>
<span data-ttu-id="f2335-146">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="f2335-146">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="f2335-147">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f2335-147">-HttpsOnly</span></span>
<span data-ttu-id="f2335-148">기존 azure web app 또는 functionapp에서 HTTPS로 모든 트래픽 리디렉션 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="f2335-148">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="f2335-149">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="f2335-149">-ManagedPipelineMode</span></span>
<span data-ttu-id="f2335-150">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="f2335-150">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="f2335-151">-이름</span><span class="sxs-lookup"><span data-stu-id="f2335-151">-Name</span></span>
<span data-ttu-id="f2335-152">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="f2335-152">WebApp Name</span></span>

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

### <span data-ttu-id="f2335-153">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="f2335-153">-NetFrameworkVersion</span></span>
<span data-ttu-id="f2335-154">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="f2335-154">Net Framework Version</span></span>

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

### <span data-ttu-id="f2335-155">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="f2335-155">-NumberOfWorkers</span></span>
<span data-ttu-id="f2335-156">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f2335-156">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="f2335-157">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="f2335-157">-PhpVersion</span></span>
<span data-ttu-id="f2335-158">Php 버전</span><span class="sxs-lookup"><span data-stu-id="f2335-158">Php Version</span></span>

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

### <span data-ttu-id="f2335-159">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="f2335-159">-RequestTracingEnabled</span></span>
<span data-ttu-id="f2335-160">요청 추적 사용</span><span class="sxs-lookup"><span data-stu-id="f2335-160">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="f2335-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2335-161">-ResourceGroupName</span></span>
<span data-ttu-id="f2335-162">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f2335-162">Resource Group Name</span></span>

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

### <span data-ttu-id="f2335-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="f2335-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="f2335-164">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="f2335-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="f2335-165">-Web app</span><span class="sxs-lookup"><span data-stu-id="f2335-165">-WebApp</span></span>
<span data-ttu-id="f2335-166">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="f2335-166">WebApp Object</span></span>

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

### <span data-ttu-id="f2335-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="f2335-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="f2335-168">WebSocketsEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="f2335-168">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="f2335-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2335-169">CommonParameters</span></span>
<span data-ttu-id="f2335-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2335-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2335-171">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2335-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2335-172">입력</span><span class="sxs-lookup"><span data-stu-id="f2335-172">INPUTS</span></span>

### <span data-ttu-id="f2335-173">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="f2335-173">System.Int32</span></span>
<span data-ttu-id="f2335-174">매개 변수: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2335-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="f2335-175">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2335-175">System.String</span></span>

### <span data-ttu-id="f2335-176">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="f2335-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="f2335-177">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2335-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="f2335-178">출력</span><span class="sxs-lookup"><span data-stu-id="f2335-178">OUTPUTS</span></span>

### <span data-ttu-id="f2335-179">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="f2335-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="f2335-180">상속자</span><span class="sxs-lookup"><span data-stu-id="f2335-180">NOTES</span></span>

## <span data-ttu-id="f2335-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2335-181">RELATED LINKS</span></span>

[<span data-ttu-id="f2335-182">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2335-182">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f2335-183">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2335-183">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="f2335-184">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2335-184">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="f2335-185">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2335-185">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="f2335-186">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2335-186">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="f2335-187">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2335-187">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
