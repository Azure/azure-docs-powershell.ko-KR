---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046506"
---
# <span data-ttu-id="de40b-101">Get-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="de40b-101">Get-AzureWebsiteLog</span></span>

## <span data-ttu-id="de40b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de40b-102">SYNOPSIS</span></span>
<span data-ttu-id="de40b-103">지정 된 웹 사이트의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-103">Gets logs for the specified website.</span></span>

## <span data-ttu-id="de40b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="de40b-104">SYNTAX</span></span>

### <span data-ttu-id="de40b-105">있음</span><span class="sxs-lookup"><span data-stu-id="de40b-105">Tail</span></span>
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="de40b-106">ListPath</span><span class="sxs-lookup"><span data-stu-id="de40b-106">ListPath</span></span>
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="de40b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="de40b-107">DESCRIPTION</span></span>
<span data-ttu-id="de40b-108">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="de40b-109">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="de40b-110">지정 된 웹 사이트의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-110">Gets log for the specified website.</span></span>

## <span data-ttu-id="de40b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="de40b-111">EXAMPLES</span></span>

### <span data-ttu-id="de40b-112">예제 1: 스트리밍 로그 시작</span><span class="sxs-lookup"><span data-stu-id="de40b-112">Example 1: Start log streaming</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail
```

<span data-ttu-id="de40b-113">이 예제에서는 모든 응용 프로그램 로그에 대 한 로깅 스트리밍을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-113">This example starts log streaming for all application logs.</span></span>

### <span data-ttu-id="de40b-114">예제 2: http 로그에 대 한 스트리밍 로그 시작</span><span class="sxs-lookup"><span data-stu-id="de40b-114">Example 2: Start log streaming for http logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

<span data-ttu-id="de40b-115">이 예제에서는 http 로그에 대 한 로그 스트리밍을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-115">This example starts log streaming for http logs.</span></span>

### <span data-ttu-id="de40b-116">예제 3: 오류 로그에 대 한 스트리밍 로그 시작</span><span class="sxs-lookup"><span data-stu-id="de40b-116">Example 3: Start log streaming for error logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

<span data-ttu-id="de40b-117">이 예제에서는 로그 스트리밍을 시작 하 고 오류 로그만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-117">This example starts log streaming and show error logs only.</span></span>

### <span data-ttu-id="de40b-118">예제 4: avaiable 로그 표시</span><span class="sxs-lookup"><span data-stu-id="de40b-118">Example 4: Display avaiable logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

<span data-ttu-id="de40b-119">이 예제에서는 웹 사이트에서 사용할 수 있는 모든 로그 경로를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-119">This example lists all available log paths in the website.</span></span>

## <span data-ttu-id="de40b-120">변수</span><span class="sxs-lookup"><span data-stu-id="de40b-120">PARAMETERS</span></span>

### <span data-ttu-id="de40b-121">-ListPath</span><span class="sxs-lookup"><span data-stu-id="de40b-121">-ListPath</span></span>
<span data-ttu-id="de40b-122">로그 경로를 나열할 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-122">Indicates whether to list the log paths.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de40b-123">-메시지</span><span class="sxs-lookup"><span data-stu-id="de40b-123">-Message</span></span>
<span data-ttu-id="de40b-124">로그 메시지를 필터링 하는 데 사용 되는 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-124">Specifies a string which will be used to filter the log message.</span></span>
<span data-ttu-id="de40b-125">이 문자열이 포함 된 로그만 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-125">Only logs which contains this string will be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de40b-126">-이름</span><span class="sxs-lookup"><span data-stu-id="de40b-126">-Name</span></span>
<span data-ttu-id="de40b-127">웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-127">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de40b-128">-Path</span><span class="sxs-lookup"><span data-stu-id="de40b-128">-Path</span></span>
<span data-ttu-id="de40b-129">로그를 검색 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-129">The path from which the log will be retrieved.</span></span>
<span data-ttu-id="de40b-130">기본적으로 루트 이며, 모든 경로가 포함 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-130">By default it is Root, which means include all the paths.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de40b-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="de40b-131">-Profile</span></span>
<span data-ttu-id="de40b-132">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="de40b-133">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de40b-134">-슬롯</span><span class="sxs-lookup"><span data-stu-id="de40b-134">-Slot</span></span>
<span data-ttu-id="de40b-135">슬롯 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-135">Specifies the slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de40b-136">-꼬리</span><span class="sxs-lookup"><span data-stu-id="de40b-136">-Tail</span></span>
<span data-ttu-id="de40b-137">로그를 스트림할 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-137">Specifies whether to stream the logs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de40b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de40b-138">CommonParameters</span></span>
<span data-ttu-id="de40b-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="de40b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de40b-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de40b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de40b-141">입력</span><span class="sxs-lookup"><span data-stu-id="de40b-141">INPUTS</span></span>

## <span data-ttu-id="de40b-142">출력</span><span class="sxs-lookup"><span data-stu-id="de40b-142">OUTPUTS</span></span>

## <span data-ttu-id="de40b-143">상속자</span><span class="sxs-lookup"><span data-stu-id="de40b-143">NOTES</span></span>

## <span data-ttu-id="de40b-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de40b-144">RELATED LINKS</span></span>

[<span data-ttu-id="de40b-145">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="de40b-145">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="de40b-146">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="de40b-146">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="de40b-147">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="de40b-147">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="de40b-148">시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="de40b-148">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


