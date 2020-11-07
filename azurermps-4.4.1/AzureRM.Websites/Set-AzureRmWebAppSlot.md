---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4780deac3d335060d5a3d7e262a61184b2e0c3b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702048"
---
# <span data-ttu-id="1980b-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1980b-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="1980b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1980b-102">SYNOPSIS</span></span>
<span data-ttu-id="1980b-103">Azure Web App 슬롯을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1980b-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1980b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1980b-104">SYNTAX</span></span>

### <span data-ttu-id="1980b-105">S1</span><span class="sxs-lookup"><span data-stu-id="1980b-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1980b-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="1980b-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1980b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1980b-107">DESCRIPTION</span></span>
<span data-ttu-id="1980b-108">**Set-AzureRmWebApp** Cmdlet은 Azure 웹 앱 슬롯을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1980b-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="1980b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1980b-109">EXAMPLES</span></span>

### <span data-ttu-id="1980b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1980b-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="1980b-111">이 명령은 리소스 그룹 기본값과 연결 된 웹 앱 ContosoWebApp에 해당 하는 슬롯 Slot001에 대해 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1980b-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="1980b-112">변수</span><span class="sxs-lookup"><span data-stu-id="1980b-112">PARAMETERS</span></span>

### <span data-ttu-id="1980b-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1980b-113">-AppServicePlan</span></span>
<span data-ttu-id="1980b-114">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="1980b-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="1980b-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="1980b-115">-AppSettings</span></span>
<span data-ttu-id="1980b-116">앱 설정 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="1980b-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="1980b-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="1980b-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="1980b-118">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="1980b-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="1980b-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="1980b-119">-ConnectionStrings</span></span>
<span data-ttu-id="1980b-120">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="1980b-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="1980b-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="1980b-121">-DefaultDocuments</span></span>
<span data-ttu-id="1980b-122">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="1980b-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="1980b-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1980b-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="1980b-124">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="1980b-124">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="1980b-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="1980b-125">-HandlerMappings</span></span>
<span data-ttu-id="1980b-126">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="1980b-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="1980b-127">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1980b-127">-HttpLoggingEnabled</span></span>
<span data-ttu-id="1980b-128">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="1980b-128">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="1980b-129">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="1980b-129">-ManagedPipelineMode</span></span>
<span data-ttu-id="1980b-130">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="1980b-130">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="1980b-131">-이름</span><span class="sxs-lookup"><span data-stu-id="1980b-131">-Name</span></span>
<span data-ttu-id="1980b-132">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="1980b-132">WebApp Name</span></span>

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

### <span data-ttu-id="1980b-133">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="1980b-133">-NetFrameworkVersion</span></span>
<span data-ttu-id="1980b-134">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="1980b-134">Net Framework Version</span></span>

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

### <span data-ttu-id="1980b-135">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="1980b-135">-NumberOfWorkers</span></span>
<span data-ttu-id="1980b-136">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1980b-136">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="1980b-137">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="1980b-137">-PhpVersion</span></span>
<span data-ttu-id="1980b-138">Php 버전</span><span class="sxs-lookup"><span data-stu-id="1980b-138">Php Version</span></span>

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

### <span data-ttu-id="1980b-139">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="1980b-139">-RequestTracingEnabled</span></span>
<span data-ttu-id="1980b-140">추적을 사용 하 여 부울 요청</span><span class="sxs-lookup"><span data-stu-id="1980b-140">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="1980b-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1980b-141">-ResourceGroupName</span></span>
<span data-ttu-id="1980b-142">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1980b-142">Resource Group Name</span></span>

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

### <span data-ttu-id="1980b-143">-슬롯</span><span class="sxs-lookup"><span data-stu-id="1980b-143">-Slot</span></span>
<span data-ttu-id="1980b-144">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="1980b-144">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1980b-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="1980b-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="1980b-146">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="1980b-146">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="1980b-147">-Web app</span><span class="sxs-lookup"><span data-stu-id="1980b-147">-WebApp</span></span>
<span data-ttu-id="1980b-148">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="1980b-148">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1980b-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="1980b-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="1980b-150">웹 소켓 사용 부울</span><span class="sxs-lookup"><span data-stu-id="1980b-150">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="1980b-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1980b-151">-DefaultProfile</span></span>
<span data-ttu-id="1980b-152">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1980b-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1980b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1980b-153">CommonParameters</span></span>
<span data-ttu-id="1980b-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1980b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1980b-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1980b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1980b-156">입력</span><span class="sxs-lookup"><span data-stu-id="1980b-156">INPUTS</span></span>

### <span data-ttu-id="1980b-157">Int32</span><span class="sxs-lookup"><span data-stu-id="1980b-157">Int32</span></span>
<span data-ttu-id="1980b-158">' NumberOfWorkers ' 매개 변수는 파이프라인에서 ' Int32 ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1980b-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="1980b-159">Site</span><span class="sxs-lookup"><span data-stu-id="1980b-159">Site</span></span>
<span data-ttu-id="1980b-160">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1980b-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1980b-161">출력</span><span class="sxs-lookup"><span data-stu-id="1980b-161">OUTPUTS</span></span>

## <span data-ttu-id="1980b-162">상속자</span><span class="sxs-lookup"><span data-stu-id="1980b-162">NOTES</span></span>

## <span data-ttu-id="1980b-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1980b-163">RELATED LINKS</span></span>

[<span data-ttu-id="1980b-164">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1980b-164">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="1980b-165">새로운 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1980b-165">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="1980b-166">제거-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1980b-166">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="1980b-167">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1980b-167">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="1980b-168">시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1980b-168">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="1980b-169">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1980b-169">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="1980b-170">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1980b-170">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
