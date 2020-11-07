---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: b6cb41e49695fa7fd9fa0efdefdbefb2b23229a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876101"
---
# <span data-ttu-id="66b5a-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66b5a-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="66b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="66b5a-103">Azure Web App 슬롯을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b5a-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="66b5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66b5a-104">SYNTAX</span></span>

### <span data-ttu-id="66b5a-105">S1</span><span class="sxs-lookup"><span data-stu-id="66b5a-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66b5a-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="66b5a-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66b5a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="66b5a-107">DESCRIPTION</span></span>
<span data-ttu-id="66b5a-108">**Set-AzWebApp** Cmdlet은 Azure 웹 앱 슬롯을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b5a-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="66b5a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="66b5a-109">EXAMPLES</span></span>

### <span data-ttu-id="66b5a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="66b5a-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="66b5a-111">이 명령은 리소스 그룹 기본값과 연결 된 웹 앱 ContosoWebApp에 해당 하는 슬롯 Slot001에 대해 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b5a-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="66b5a-112">변수</span><span class="sxs-lookup"><span data-stu-id="66b5a-112">PARAMETERS</span></span>

### <span data-ttu-id="66b5a-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="66b5a-113">-AppServicePlan</span></span>
<span data-ttu-id="66b5a-114">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="66b5a-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="66b5a-115">-AppSettings</span></span>
<span data-ttu-id="66b5a-116">앱 설정 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="66b5a-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="66b5a-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="66b5a-118">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="66b5a-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="66b5a-119">-ConnectionStrings</span></span>
<span data-ttu-id="66b5a-120">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="66b5a-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="66b5a-121">-DefaultDocuments</span></span>
<span data-ttu-id="66b5a-122">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="66b5a-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b5a-123">-DefaultProfile</span></span>
<span data-ttu-id="66b5a-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66b5a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b5a-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="66b5a-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="66b5a-126">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="66b5a-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="66b5a-127">-HandlerMappings</span></span>
<span data-ttu-id="66b5a-128">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="66b5a-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="66b5a-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="66b5a-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="66b5a-130">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="66b5a-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="66b5a-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="66b5a-132">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="66b5a-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-133">-이름</span><span class="sxs-lookup"><span data-stu-id="66b5a-133">-Name</span></span>
<span data-ttu-id="66b5a-134">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="66b5a-134">WebApp Name</span></span>

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

### <span data-ttu-id="66b5a-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="66b5a-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="66b5a-136">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="66b5a-136">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="66b5a-137">-NumberOfWorkers</span></span>
<span data-ttu-id="66b5a-138">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="66b5a-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="66b5a-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="66b5a-139">-PhpVersion</span></span>
<span data-ttu-id="66b5a-140">Php 버전</span><span class="sxs-lookup"><span data-stu-id="66b5a-140">Php Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="66b5a-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="66b5a-142">추적을 사용 하 여 부울 요청</span><span class="sxs-lookup"><span data-stu-id="66b5a-142">Request Tracing Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b5a-143">-ResourceGroupName</span></span>
<span data-ttu-id="66b5a-144">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="66b5a-144">Resource Group Name</span></span>

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

### <span data-ttu-id="66b5a-145">-슬롯</span><span class="sxs-lookup"><span data-stu-id="66b5a-145">-Slot</span></span>
<span data-ttu-id="66b5a-146">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="66b5a-146">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="66b5a-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="66b5a-148">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="66b5a-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5a-149">-Web app</span><span class="sxs-lookup"><span data-stu-id="66b5a-149">-WebApp</span></span>
<span data-ttu-id="66b5a-150">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="66b5a-150">WebApp Object</span></span>

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

### <span data-ttu-id="66b5a-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="66b5a-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="66b5a-152">웹 소켓 사용 부울</span><span class="sxs-lookup"><span data-stu-id="66b5a-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="66b5a-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="66b5a-153">-HttpsOnly</span></span>
<span data-ttu-id="66b5a-154">기존 슬롯에서 모든 트래픽을 HTTPS로 리디렉션하는 기능 설정/해제</span><span class="sxs-lookup"><span data-stu-id="66b5a-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="66b5a-155">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="66b5a-155">-AssignIdentity</span></span>
<span data-ttu-id="66b5a-156">기존 슬롯에서 MSI 사용/사용 안 함 [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="66b5a-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="66b5a-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66b5a-157">-AsJob</span></span>
<span data-ttu-id="66b5a-158">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="66b5a-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66b5a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b5a-159">CommonParameters</span></span>
<span data-ttu-id="66b5a-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b5a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b5a-161">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b5a-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b5a-162">입력</span><span class="sxs-lookup"><span data-stu-id="66b5a-162">INPUTS</span></span>

### <span data-ttu-id="66b5a-163">Int32</span><span class="sxs-lookup"><span data-stu-id="66b5a-163">Int32</span></span>
<span data-ttu-id="66b5a-164">' NumberOfWorkers ' 매개 변수는 파이프라인에서 ' Int32 ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b5a-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="66b5a-165">Site</span><span class="sxs-lookup"><span data-stu-id="66b5a-165">Site</span></span>
<span data-ttu-id="66b5a-166">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="66b5a-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="66b5a-167">출력</span><span class="sxs-lookup"><span data-stu-id="66b5a-167">OUTPUTS</span></span>

## <span data-ttu-id="66b5a-168">상속자</span><span class="sxs-lookup"><span data-stu-id="66b5a-168">NOTES</span></span>

## <span data-ttu-id="66b5a-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66b5a-169">RELATED LINKS</span></span>

[<span data-ttu-id="66b5a-170">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66b5a-170">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="66b5a-171">새로운 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66b5a-171">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="66b5a-172">제거-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66b5a-172">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="66b5a-173">다시 시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66b5a-173">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="66b5a-174">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66b5a-174">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="66b5a-175">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66b5a-175">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="66b5a-176">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="66b5a-176">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
