---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 16a60f5f9951aaa40ac8da8584e1c2690206cdb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536856"
---
# <span data-ttu-id="0c6e0-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0c6e0-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="0c6e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c6e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6e0-103">API Management로 거를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c6e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c6e0-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c6e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0c6e0-105">DESCRIPTION</span></span>
<span data-ttu-id="0c6e0-106">**Set-AzureRmApiManagementLogger** Cmdlet은 Azure API Management **로 거** 의 설정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="0c6e0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0c6e0-107">EXAMPLES</span></span>

### <span data-ttu-id="0c6e0-108">예제 1:로 거 수정</span><span class="sxs-lookup"><span data-stu-id="0c6e0-108">Example 1: Modify a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="0c6e0-109">이 명령은 ID Logger123 인로 거를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="0c6e0-110">변수</span><span class="sxs-lookup"><span data-stu-id="0c6e0-110">PARAMETERS</span></span>

### <span data-ttu-id="0c6e0-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="0c6e0-111">-ConnectionString</span></span>
<span data-ttu-id="0c6e0-112">정책 보내기 권한이 포함 된 Azure 이벤트 허브 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="0c6e0-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="0c6e0-113">-Context</span></span>
<span data-ttu-id="0c6e0-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6e0-115">-DefaultProfile</span></span>
<span data-ttu-id="0c6e0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0c6e0-117">-설명</span><span class="sxs-lookup"><span data-stu-id="0c6e0-117">-Description</span></span>
<span data-ttu-id="0c6e0-118">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-118">Specifies a description.</span></span>

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

### <span data-ttu-id="0c6e0-119">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="0c6e0-119">-IsBuffered</span></span>
<span data-ttu-id="0c6e0-120">게시 하기 전에로 거의 레코드를 버퍼링 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-120">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="0c6e0-121">레코드가 버퍼링 되 면 15 초 마다 이벤트 허브에 또는 버퍼가 256 KB의 메시지를 받을 때마다 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6e0-122">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="0c6e0-122">-LoggerId</span></span>
<span data-ttu-id="0c6e0-123">업데이트할로 거의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-123">Specifies the ID of the logger to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6e0-124">-이름</span><span class="sxs-lookup"><span data-stu-id="0c6e0-124">-Name</span></span>
<span data-ttu-id="0c6e0-125">Azure 클래식 포털에서 이벤트 허브의 엔터티 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-125">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="0c6e0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c6e0-126">-PassThru</span></span>
<span data-ttu-id="0c6e0-127">이 cmdlet이이 cmdlet이 수정 하는  **PsApiManagementLogger** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-127">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6e0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6e0-128">CommonParameters</span></span>
<span data-ttu-id="0c6e0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6e0-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c6e0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6e0-131">입력</span><span class="sxs-lookup"><span data-stu-id="0c6e0-131">INPUTS</span></span>

### <span data-ttu-id="0c6e0-132">않아야</span><span class="sxs-lookup"><span data-stu-id="0c6e0-132">None</span></span>
<span data-ttu-id="0c6e0-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0c6e0-134">출력</span><span class="sxs-lookup"><span data-stu-id="0c6e0-134">OUTPUTS</span></span>

### <span data-ttu-id="0c6e0-135">ApiManagement. ServiceManagement. \ PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0c6e0-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="0c6e0-136">상속자</span><span class="sxs-lookup"><span data-stu-id="0c6e0-136">NOTES</span></span>

## <span data-ttu-id="0c6e0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c6e0-137">RELATED LINKS</span></span>

[<span data-ttu-id="0c6e0-138">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0c6e0-138">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="0c6e0-139">새로운 AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0c6e0-139">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="0c6e0-140">제거-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0c6e0-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


