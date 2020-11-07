---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 245ce5ab011f03b8d8331b5d80fa4eeb01e19e15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882414"
---
# <span data-ttu-id="051cb-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="051cb-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="051cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="051cb-102">SYNOPSIS</span></span>
<span data-ttu-id="051cb-103">Azure Web App 슬롯을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="051cb-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="051cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="051cb-104">SYNTAX</span></span>

### <span data-ttu-id="051cb-105">S1</span><span class="sxs-lookup"><span data-stu-id="051cb-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="051cb-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="051cb-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="051cb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="051cb-107">DESCRIPTION</span></span>
<span data-ttu-id="051cb-108">**Set-AzureRmWebApp** Cmdlet은 Azure 웹 앱 슬롯을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="051cb-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="051cb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="051cb-109">EXAMPLES</span></span>

### <span data-ttu-id="051cb-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="051cb-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="051cb-111">이 명령은 리소스 그룹 기본값과 연결 된 웹 앱 ContosoWebApp에 해당 하는 슬롯 Slot001에 대해 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="051cb-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="051cb-112">변수</span><span class="sxs-lookup"><span data-stu-id="051cb-112">PARAMETERS</span></span>

### <span data-ttu-id="051cb-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="051cb-113">-AppServicePlan</span></span>
<span data-ttu-id="051cb-114">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="051cb-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="051cb-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="051cb-115">-AppSettings</span></span>
<span data-ttu-id="051cb-116">앱 설정 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="051cb-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="051cb-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="051cb-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="051cb-118">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="051cb-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="051cb-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="051cb-119">-ConnectionStrings</span></span>
<span data-ttu-id="051cb-120">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="051cb-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="051cb-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="051cb-121">-DefaultDocuments</span></span>
<span data-ttu-id="051cb-122">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="051cb-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="051cb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="051cb-123">-DefaultProfile</span></span>
<span data-ttu-id="051cb-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="051cb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051cb-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="051cb-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="051cb-126">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="051cb-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="051cb-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="051cb-127">-HandlerMappings</span></span>
<span data-ttu-id="051cb-128">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="051cb-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="051cb-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="051cb-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="051cb-130">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="051cb-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="051cb-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="051cb-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="051cb-132">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="051cb-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="051cb-133">-이름</span><span class="sxs-lookup"><span data-stu-id="051cb-133">-Name</span></span>
<span data-ttu-id="051cb-134">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="051cb-134">WebApp Name</span></span>

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

### <span data-ttu-id="051cb-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="051cb-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="051cb-136">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="051cb-136">Net Framework Version</span></span>

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

### <span data-ttu-id="051cb-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="051cb-137">-NumberOfWorkers</span></span>
<span data-ttu-id="051cb-138">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="051cb-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="051cb-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="051cb-139">-PhpVersion</span></span>
<span data-ttu-id="051cb-140">Php 버전</span><span class="sxs-lookup"><span data-stu-id="051cb-140">Php Version</span></span>

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

### <span data-ttu-id="051cb-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="051cb-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="051cb-142">추적을 사용 하 여 부울 요청</span><span class="sxs-lookup"><span data-stu-id="051cb-142">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="051cb-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="051cb-143">-ResourceGroupName</span></span>
<span data-ttu-id="051cb-144">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="051cb-144">Resource Group Name</span></span>

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

### <span data-ttu-id="051cb-145">-슬롯</span><span class="sxs-lookup"><span data-stu-id="051cb-145">-Slot</span></span>
<span data-ttu-id="051cb-146">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="051cb-146">WebApp Slot Name</span></span>

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

### <span data-ttu-id="051cb-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="051cb-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="051cb-148">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="051cb-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="051cb-149">-Web app</span><span class="sxs-lookup"><span data-stu-id="051cb-149">-WebApp</span></span>
<span data-ttu-id="051cb-150">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="051cb-150">WebApp Object</span></span>

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

### <span data-ttu-id="051cb-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="051cb-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="051cb-152">웹 소켓 사용 부울</span><span class="sxs-lookup"><span data-stu-id="051cb-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="051cb-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="051cb-153">-HttpsOnly</span></span>
<span data-ttu-id="051cb-154">기존 슬롯에서 모든 트래픽을 HTTPS로 리디렉션하는 기능 설정/해제</span><span class="sxs-lookup"><span data-stu-id="051cb-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="051cb-155">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="051cb-155">-AssignIdentity</span></span>
<span data-ttu-id="051cb-156">기존 슬롯에서 MSI 사용/사용 안 함 [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="051cb-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="051cb-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="051cb-157">-AsJob</span></span>
<span data-ttu-id="051cb-158">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="051cb-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="051cb-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="051cb-159">CommonParameters</span></span>
<span data-ttu-id="051cb-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="051cb-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="051cb-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="051cb-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="051cb-162">입력</span><span class="sxs-lookup"><span data-stu-id="051cb-162">INPUTS</span></span>

### <span data-ttu-id="051cb-163">Int32</span><span class="sxs-lookup"><span data-stu-id="051cb-163">Int32</span></span>
<span data-ttu-id="051cb-164">' NumberOfWorkers ' 매개 변수는 파이프라인에서 ' Int32 ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="051cb-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="051cb-165">Site</span><span class="sxs-lookup"><span data-stu-id="051cb-165">Site</span></span>
<span data-ttu-id="051cb-166">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="051cb-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="051cb-167">출력</span><span class="sxs-lookup"><span data-stu-id="051cb-167">OUTPUTS</span></span>

## <span data-ttu-id="051cb-168">상속자</span><span class="sxs-lookup"><span data-stu-id="051cb-168">NOTES</span></span>

## <span data-ttu-id="051cb-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="051cb-169">RELATED LINKS</span></span>

[<span data-ttu-id="051cb-170">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="051cb-170">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="051cb-171">새로운 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="051cb-171">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="051cb-172">제거-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="051cb-172">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="051cb-173">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="051cb-173">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="051cb-174">시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="051cb-174">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="051cb-175">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="051cb-175">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="051cb-176">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="051cb-176">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
