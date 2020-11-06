---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 0f8008a2b567bb2cb2b67755d2ea5bb586f0c115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528172"
---
# <span data-ttu-id="2017e-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2017e-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="2017e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2017e-102">SYNOPSIS</span></span>
<span data-ttu-id="2017e-103">Azure Web App을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2017e-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2017e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2017e-104">SYNTAX</span></span>

### <span data-ttu-id="2017e-105">S1</span><span class="sxs-lookup"><span data-stu-id="2017e-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2017e-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="2017e-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2017e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2017e-107">DESCRIPTION</span></span>
<span data-ttu-id="2017e-108">**AzureRmWebApp** Cmdlet은 Azure 웹 앱을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2017e-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="2017e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2017e-109">EXAMPLES</span></span>

### <span data-ttu-id="2017e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2017e-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="2017e-111">이 명령은 리소스 그룹 Default-웹에 연결 된 웹 앱 ContosoWebApp에 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2017e-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2017e-112">변수</span><span class="sxs-lookup"><span data-stu-id="2017e-112">PARAMETERS</span></span>

### <span data-ttu-id="2017e-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2017e-113">-AppServicePlan</span></span>
<span data-ttu-id="2017e-114">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="2017e-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="2017e-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="2017e-115">-AppSettings</span></span>
<span data-ttu-id="2017e-116">앱 설정 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="2017e-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="2017e-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="2017e-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="2017e-118">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="2017e-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="2017e-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="2017e-119">-ConnectionStrings</span></span>
<span data-ttu-id="2017e-120">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="2017e-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="2017e-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="2017e-121">-DefaultDocuments</span></span>
<span data-ttu-id="2017e-122">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="2017e-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="2017e-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2017e-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="2017e-124">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="2017e-124">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="2017e-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="2017e-125">-HandlerMappings</span></span>
<span data-ttu-id="2017e-126">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="2017e-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="2017e-127">-호스트 이름</span><span class="sxs-lookup"><span data-stu-id="2017e-127">-HostNames</span></span>
<span data-ttu-id="2017e-128">Web app 호스트 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="2017e-128">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="2017e-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2017e-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="2017e-130">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="2017e-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="2017e-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="2017e-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="2017e-132">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="2017e-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="2017e-133">-이름</span><span class="sxs-lookup"><span data-stu-id="2017e-133">-Name</span></span>
<span data-ttu-id="2017e-134">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="2017e-134">WebApp Name</span></span>

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

### <span data-ttu-id="2017e-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="2017e-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="2017e-136">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="2017e-136">Net Framework Version</span></span>

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

### <span data-ttu-id="2017e-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="2017e-137">-NumberOfWorkers</span></span>
<span data-ttu-id="2017e-138">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2017e-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="2017e-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="2017e-139">-PhpVersion</span></span>
<span data-ttu-id="2017e-140">Php 버전</span><span class="sxs-lookup"><span data-stu-id="2017e-140">Php Version</span></span>

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

### <span data-ttu-id="2017e-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="2017e-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="2017e-142">요청 추적 사용</span><span class="sxs-lookup"><span data-stu-id="2017e-142">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="2017e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2017e-143">-ResourceGroupName</span></span>
<span data-ttu-id="2017e-144">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2017e-144">Resource Group Name</span></span>

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

### <span data-ttu-id="2017e-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="2017e-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="2017e-146">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="2017e-146">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="2017e-147">-Web app</span><span class="sxs-lookup"><span data-stu-id="2017e-147">-WebApp</span></span>
<span data-ttu-id="2017e-148">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="2017e-148">WebApp Object</span></span>

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

### <span data-ttu-id="2017e-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="2017e-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="2017e-150">WebSocketsEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="2017e-150">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="2017e-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2017e-151">-DefaultProfile</span></span>
<span data-ttu-id="2017e-152">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2017e-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2017e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2017e-153">CommonParameters</span></span>
<span data-ttu-id="2017e-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2017e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2017e-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2017e-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2017e-156">입력</span><span class="sxs-lookup"><span data-stu-id="2017e-156">INPUTS</span></span>

### <span data-ttu-id="2017e-157">Int32</span><span class="sxs-lookup"><span data-stu-id="2017e-157">Int32</span></span>
<span data-ttu-id="2017e-158">' NumberOfWorkers ' 매개 변수는 파이프라인에서 ' Int32 ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2017e-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="2017e-159">Site</span><span class="sxs-lookup"><span data-stu-id="2017e-159">Site</span></span>
<span data-ttu-id="2017e-160">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2017e-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2017e-161">출력</span><span class="sxs-lookup"><span data-stu-id="2017e-161">OUTPUTS</span></span>

## <span data-ttu-id="2017e-162">상속자</span><span class="sxs-lookup"><span data-stu-id="2017e-162">NOTES</span></span>

## <span data-ttu-id="2017e-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2017e-163">RELATED LINKS</span></span>

[<span data-ttu-id="2017e-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2017e-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="2017e-165">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2017e-165">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="2017e-166">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2017e-166">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="2017e-167">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2017e-167">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="2017e-168">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2017e-168">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="2017e-169">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2017e-169">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
