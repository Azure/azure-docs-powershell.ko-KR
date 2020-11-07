---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 717f355326acc4d169bee1e93d98446fa052a5e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703934"
---
# <span data-ttu-id="bef2c-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bef2c-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="bef2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bef2c-102">SYNOPSIS</span></span>
<span data-ttu-id="bef2c-103">Azure Web App 슬롯을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bef2c-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bef2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bef2c-104">SYNTAX</span></span>

### <span data-ttu-id="bef2c-105">S1</span><span class="sxs-lookup"><span data-stu-id="bef2c-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bef2c-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="bef2c-106">S2</span></span>
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

## <span data-ttu-id="bef2c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bef2c-107">DESCRIPTION</span></span>
<span data-ttu-id="bef2c-108">**Set-AzureRmWebApp** Cmdlet은 Azure 웹 앱 슬롯을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bef2c-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="bef2c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bef2c-109">EXAMPLES</span></span>

### <span data-ttu-id="bef2c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bef2c-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="bef2c-111">이 명령은 리소스 그룹 기본값과 연결 된 웹 앱 ContosoWebApp에 해당 하는 슬롯 Slot001에 대해 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bef2c-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="bef2c-112">변수</span><span class="sxs-lookup"><span data-stu-id="bef2c-112">PARAMETERS</span></span>

### <span data-ttu-id="bef2c-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bef2c-113">-AppServicePlan</span></span>
<span data-ttu-id="bef2c-114">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="bef2c-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="bef2c-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="bef2c-115">-AppSettings</span></span>
<span data-ttu-id="bef2c-116">앱 설정 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="bef2c-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="bef2c-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="bef2c-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="bef2c-118">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="bef2c-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="bef2c-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="bef2c-119">-ConnectionStrings</span></span>
<span data-ttu-id="bef2c-120">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="bef2c-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="bef2c-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="bef2c-121">-DefaultDocuments</span></span>
<span data-ttu-id="bef2c-122">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="bef2c-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="bef2c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef2c-123">-DefaultProfile</span></span>
<span data-ttu-id="bef2c-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bef2c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bef2c-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="bef2c-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="bef2c-126">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="bef2c-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="bef2c-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="bef2c-127">-HandlerMappings</span></span>
<span data-ttu-id="bef2c-128">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="bef2c-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="bef2c-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="bef2c-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="bef2c-130">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="bef2c-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="bef2c-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="bef2c-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="bef2c-132">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="bef2c-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="bef2c-133">-이름</span><span class="sxs-lookup"><span data-stu-id="bef2c-133">-Name</span></span>
<span data-ttu-id="bef2c-134">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="bef2c-134">WebApp Name</span></span>

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

### <span data-ttu-id="bef2c-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="bef2c-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="bef2c-136">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="bef2c-136">Net Framework Version</span></span>

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

### <span data-ttu-id="bef2c-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="bef2c-137">-NumberOfWorkers</span></span>
<span data-ttu-id="bef2c-138">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bef2c-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="bef2c-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="bef2c-139">-PhpVersion</span></span>
<span data-ttu-id="bef2c-140">Php 버전</span><span class="sxs-lookup"><span data-stu-id="bef2c-140">Php Version</span></span>

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

### <span data-ttu-id="bef2c-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="bef2c-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="bef2c-142">추적을 사용 하 여 부울 요청</span><span class="sxs-lookup"><span data-stu-id="bef2c-142">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="bef2c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bef2c-143">-ResourceGroupName</span></span>
<span data-ttu-id="bef2c-144">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bef2c-144">Resource Group Name</span></span>

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

### <span data-ttu-id="bef2c-145">-슬롯</span><span class="sxs-lookup"><span data-stu-id="bef2c-145">-Slot</span></span>
<span data-ttu-id="bef2c-146">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="bef2c-146">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bef2c-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="bef2c-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="bef2c-148">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="bef2c-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="bef2c-149">-Web app</span><span class="sxs-lookup"><span data-stu-id="bef2c-149">-WebApp</span></span>
<span data-ttu-id="bef2c-150">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="bef2c-150">WebApp Object</span></span>

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

### <span data-ttu-id="bef2c-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="bef2c-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="bef2c-152">웹 소켓 사용 부울</span><span class="sxs-lookup"><span data-stu-id="bef2c-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="bef2c-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bef2c-153">-AsJob</span></span>
<span data-ttu-id="bef2c-154">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bef2c-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bef2c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef2c-155">CommonParameters</span></span>
<span data-ttu-id="bef2c-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bef2c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef2c-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bef2c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef2c-158">입력</span><span class="sxs-lookup"><span data-stu-id="bef2c-158">INPUTS</span></span>

### <span data-ttu-id="bef2c-159">Int32</span><span class="sxs-lookup"><span data-stu-id="bef2c-159">Int32</span></span>
<span data-ttu-id="bef2c-160">' NumberOfWorkers ' 매개 변수는 파이프라인에서 ' Int32 ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bef2c-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="bef2c-161">Site</span><span class="sxs-lookup"><span data-stu-id="bef2c-161">Site</span></span>
<span data-ttu-id="bef2c-162">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bef2c-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bef2c-163">출력</span><span class="sxs-lookup"><span data-stu-id="bef2c-163">OUTPUTS</span></span>

## <span data-ttu-id="bef2c-164">상속자</span><span class="sxs-lookup"><span data-stu-id="bef2c-164">NOTES</span></span>

## <span data-ttu-id="bef2c-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bef2c-165">RELATED LINKS</span></span>

[<span data-ttu-id="bef2c-166">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bef2c-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="bef2c-167">새로운 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bef2c-167">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="bef2c-168">제거-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bef2c-168">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="bef2c-169">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bef2c-169">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="bef2c-170">시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bef2c-170">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="bef2c-171">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bef2c-171">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="bef2c-172">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bef2c-172">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
