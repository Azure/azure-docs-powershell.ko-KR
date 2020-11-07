---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4478083a2ee98eceda08012b4346f3ece1657963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876102"
---
# <span data-ttu-id="488be-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="488be-101">Set-AzWebApp</span></span>

## <span data-ttu-id="488be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="488be-102">SYNOPSIS</span></span>
<span data-ttu-id="488be-103">Azure Web App을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="488be-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="488be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="488be-104">SYNTAX</span></span>

### <span data-ttu-id="488be-105">S1</span><span class="sxs-lookup"><span data-stu-id="488be-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="488be-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="488be-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="488be-107">설명은</span><span class="sxs-lookup"><span data-stu-id="488be-107">DESCRIPTION</span></span>
<span data-ttu-id="488be-108">**AzWebApp** Cmdlet은 Azure 웹 앱을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="488be-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="488be-109">예제의</span><span class="sxs-lookup"><span data-stu-id="488be-109">EXAMPLES</span></span>

### <span data-ttu-id="488be-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="488be-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="488be-111">이 명령은 리소스 그룹 Default-웹에 연결 된 웹 앱 ContosoWebApp에 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="488be-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="488be-112">변수</span><span class="sxs-lookup"><span data-stu-id="488be-112">PARAMETERS</span></span>

### <span data-ttu-id="488be-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="488be-113">-AppServicePlan</span></span>
<span data-ttu-id="488be-114">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="488be-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="488be-115">-AppSettings</span></span>
<span data-ttu-id="488be-116">앱 설정 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="488be-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="488be-117">-AsJob</span></span>
<span data-ttu-id="488be-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="488be-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-119">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="488be-119">-AssignIdentity</span></span>
<span data-ttu-id="488be-120">기존 azure web app 또는 functionapp [PREVIEW]에서 MSI 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="488be-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="488be-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="488be-122">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="488be-122">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="488be-123">-ConnectionStrings</span></span>
<span data-ttu-id="488be-124">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="488be-124">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="488be-125">-DefaultDocuments</span></span>
<span data-ttu-id="488be-126">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="488be-126">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="488be-127">-DefaultProfile</span></span>
<span data-ttu-id="488be-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="488be-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="488be-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="488be-130">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="488be-130">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="488be-131">-HandlerMappings</span></span>
<span data-ttu-id="488be-132">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="488be-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="488be-133">-호스트 이름</span><span class="sxs-lookup"><span data-stu-id="488be-133">-HostNames</span></span>
<span data-ttu-id="488be-134">Web app 호스트 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="488be-134">WebApp HostNames String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="488be-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="488be-136">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="488be-136">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="488be-137">-HttpsOnly</span></span>
<span data-ttu-id="488be-138">기존 azure web app 또는 functionapp에서 HTTPS로 모든 트래픽 리디렉션 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="488be-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="488be-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="488be-140">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="488be-140">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-141">-이름</span><span class="sxs-lookup"><span data-stu-id="488be-141">-Name</span></span>
<span data-ttu-id="488be-142">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="488be-142">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="488be-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="488be-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="488be-144">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="488be-144">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="488be-145">-NumberOfWorkers</span></span>
<span data-ttu-id="488be-146">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="488be-146">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="488be-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="488be-147">-PhpVersion</span></span>
<span data-ttu-id="488be-148">Php 버전</span><span class="sxs-lookup"><span data-stu-id="488be-148">Php Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="488be-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="488be-150">요청 추적 사용</span><span class="sxs-lookup"><span data-stu-id="488be-150">Request Tracing Enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="488be-151">-ResourceGroupName</span></span>
<span data-ttu-id="488be-152">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="488be-152">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="488be-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="488be-154">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="488be-154">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-155">-Web app</span><span class="sxs-lookup"><span data-stu-id="488be-155">-WebApp</span></span>
<span data-ttu-id="488be-156">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="488be-156">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="488be-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="488be-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="488be-158">WebSocketsEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="488be-158">WebSocketsEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488be-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="488be-159">CommonParameters</span></span>
<span data-ttu-id="488be-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="488be-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="488be-161">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="488be-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="488be-162">입력</span><span class="sxs-lookup"><span data-stu-id="488be-162">INPUTS</span></span>

### <span data-ttu-id="488be-163">Int32</span><span class="sxs-lookup"><span data-stu-id="488be-163">Int32</span></span>
<span data-ttu-id="488be-164">' NumberOfWorkers ' 매개 변수는 파이프라인에서 ' Int32 ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="488be-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="488be-165">Site</span><span class="sxs-lookup"><span data-stu-id="488be-165">Site</span></span>
<span data-ttu-id="488be-166">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="488be-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="488be-167">출력</span><span class="sxs-lookup"><span data-stu-id="488be-167">OUTPUTS</span></span>

## <span data-ttu-id="488be-168">상속자</span><span class="sxs-lookup"><span data-stu-id="488be-168">NOTES</span></span>

## <span data-ttu-id="488be-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="488be-169">RELATED LINKS</span></span>

[<span data-ttu-id="488be-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="488be-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="488be-171">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="488be-171">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="488be-172">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="488be-172">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="488be-173">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="488be-173">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="488be-174">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="488be-174">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="488be-175">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="488be-175">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
