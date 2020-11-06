---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 3587c7a725386976a04a9dc9922b3b0a16eb9362
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534535"
---
# <span data-ttu-id="1251f-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1251f-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="1251f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1251f-102">SYNOPSIS</span></span>
<span data-ttu-id="1251f-103">Azure Web App을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1251f-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1251f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1251f-104">SYNTAX</span></span>

### <span data-ttu-id="1251f-105">S1</span><span class="sxs-lookup"><span data-stu-id="1251f-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1251f-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="1251f-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1251f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1251f-107">DESCRIPTION</span></span>
<span data-ttu-id="1251f-108">**AzureRmWebApp** Cmdlet은 Azure 웹 앱을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1251f-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="1251f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1251f-109">EXAMPLES</span></span>

### <span data-ttu-id="1251f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1251f-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="1251f-111">이 명령은 리소스 그룹 Default-웹에 연결 된 웹 앱 ContosoWebApp에 HttpLoggingEnabled를 true로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1251f-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="1251f-112">변수</span><span class="sxs-lookup"><span data-stu-id="1251f-112">PARAMETERS</span></span>

### <span data-ttu-id="1251f-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1251f-113">-AppServicePlan</span></span>
<span data-ttu-id="1251f-114">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="1251f-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="1251f-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="1251f-115">-AppSettings</span></span>
<span data-ttu-id="1251f-116">앱 설정 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="1251f-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="1251f-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="1251f-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="1251f-118">자동 바꾸기의 대상 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="1251f-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="1251f-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="1251f-119">-ConnectionStrings</span></span>
<span data-ttu-id="1251f-120">연결 문자열 해시 테이블</span><span class="sxs-lookup"><span data-stu-id="1251f-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="1251f-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="1251f-121">-DefaultDocuments</span></span>
<span data-ttu-id="1251f-122">기본 문서 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="1251f-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="1251f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1251f-123">-DefaultProfile</span></span>
<span data-ttu-id="1251f-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1251f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1251f-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1251f-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="1251f-126">자세한 오류 로깅 사용 부울</span><span class="sxs-lookup"><span data-stu-id="1251f-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="1251f-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="1251f-127">-HandlerMappings</span></span>
<span data-ttu-id="1251f-128">처리기 매핑 IList</span><span class="sxs-lookup"><span data-stu-id="1251f-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="1251f-129">-호스트 이름</span><span class="sxs-lookup"><span data-stu-id="1251f-129">-HostNames</span></span>
<span data-ttu-id="1251f-130">Web app 호스트 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="1251f-130">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="1251f-131">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1251f-131">-HttpLoggingEnabled</span></span>
<span data-ttu-id="1251f-132">HttpLoggingEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="1251f-132">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="1251f-133">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="1251f-133">-ManagedPipelineMode</span></span>
<span data-ttu-id="1251f-134">관리 되는 파이프라인 모드 이름</span><span class="sxs-lookup"><span data-stu-id="1251f-134">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="1251f-135">-이름</span><span class="sxs-lookup"><span data-stu-id="1251f-135">-Name</span></span>
<span data-ttu-id="1251f-136">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="1251f-136">WebApp Name</span></span>

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

### <span data-ttu-id="1251f-137">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="1251f-137">-NetFrameworkVersion</span></span>
<span data-ttu-id="1251f-138">Net Framework 버전</span><span class="sxs-lookup"><span data-stu-id="1251f-138">Net Framework Version</span></span>

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

### <span data-ttu-id="1251f-139">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="1251f-139">-NumberOfWorkers</span></span>
<span data-ttu-id="1251f-140">할당할 작업자의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1251f-140">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="1251f-141">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="1251f-141">-PhpVersion</span></span>
<span data-ttu-id="1251f-142">Php 버전</span><span class="sxs-lookup"><span data-stu-id="1251f-142">Php Version</span></span>

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

### <span data-ttu-id="1251f-143">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="1251f-143">-RequestTracingEnabled</span></span>
<span data-ttu-id="1251f-144">요청 추적 사용</span><span class="sxs-lookup"><span data-stu-id="1251f-144">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="1251f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1251f-145">-ResourceGroupName</span></span>
<span data-ttu-id="1251f-146">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1251f-146">Resource Group Name</span></span>

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

### <span data-ttu-id="1251f-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="1251f-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="1251f-148">32 비트 작업자 프로세스 부울 사용</span><span class="sxs-lookup"><span data-stu-id="1251f-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="1251f-149">-Web app</span><span class="sxs-lookup"><span data-stu-id="1251f-149">-WebApp</span></span>
<span data-ttu-id="1251f-150">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="1251f-150">WebApp Object</span></span>

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

### <span data-ttu-id="1251f-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="1251f-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="1251f-152">WebSocketsEnabled 부울</span><span class="sxs-lookup"><span data-stu-id="1251f-152">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="1251f-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1251f-153">-AsJob</span></span>
<span data-ttu-id="1251f-154">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1251f-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1251f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1251f-155">CommonParameters</span></span>
<span data-ttu-id="1251f-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1251f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1251f-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1251f-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1251f-158">입력</span><span class="sxs-lookup"><span data-stu-id="1251f-158">INPUTS</span></span>

### <span data-ttu-id="1251f-159">Int32</span><span class="sxs-lookup"><span data-stu-id="1251f-159">Int32</span></span>
<span data-ttu-id="1251f-160">' NumberOfWorkers ' 매개 변수는 파이프라인에서 ' Int32 ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1251f-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="1251f-161">Site</span><span class="sxs-lookup"><span data-stu-id="1251f-161">Site</span></span>
<span data-ttu-id="1251f-162">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1251f-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1251f-163">출력</span><span class="sxs-lookup"><span data-stu-id="1251f-163">OUTPUTS</span></span>

## <span data-ttu-id="1251f-164">상속자</span><span class="sxs-lookup"><span data-stu-id="1251f-164">NOTES</span></span>

## <span data-ttu-id="1251f-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1251f-165">RELATED LINKS</span></span>

[<span data-ttu-id="1251f-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1251f-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="1251f-167">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1251f-167">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="1251f-168">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1251f-168">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="1251f-169">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1251f-169">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="1251f-170">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1251f-170">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="1251f-171">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1251f-171">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
