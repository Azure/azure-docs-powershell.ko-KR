---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2929cbd89328d971b47b748d4aa042ade13c1af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529946"
---
# <span data-ttu-id="82ec2-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="82ec2-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="82ec2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="82ec2-103">API Management로 거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ec2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82ec2-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82ec2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="82ec2-105">DESCRIPTION</span></span>
<span data-ttu-id="82ec2-106">**AzureRmApiManagementLogger** Cmdlet은 Azure API Management **로 거** 를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="82ec2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="82ec2-107">EXAMPLES</span></span>

### <span data-ttu-id="82ec2-108">예제 1:로 거 만들기</span><span class="sxs-lookup"><span data-stu-id="82ec2-108">Example 1: Create a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="82ec2-109">이 명령은 지정 된 연결 문자열을 사용 하 여 ContosoSdkEventHub 이라는로 거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="82ec2-110">변수</span><span class="sxs-lookup"><span data-stu-id="82ec2-110">PARAMETERS</span></span>

### <span data-ttu-id="82ec2-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="82ec2-111">-ConnectionString</span></span>
<span data-ttu-id="82ec2-112">다음으로 시작 하는 Azure 이벤트 허브 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="82ec2-113">연결 문자열에서 전송 권한이 있는 키를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-113">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="82ec2-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="82ec2-114">-Context</span></span>
<span data-ttu-id="82ec2-115">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="82ec2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ec2-116">-DefaultProfile</span></span>
<span data-ttu-id="82ec2-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="82ec2-118">-설명</span><span class="sxs-lookup"><span data-stu-id="82ec2-118">-Description</span></span>
<span data-ttu-id="82ec2-119">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-119">Specifies a description.</span></span>

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

### <span data-ttu-id="82ec2-120">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="82ec2-120">-IsBuffered</span></span>
<span data-ttu-id="82ec2-121">게시 하기 전에로 거의 레코드를 버퍼링 할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-121">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="82ec2-122">기본값은 $True입니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-122">The default value is $True.</span></span>
<span data-ttu-id="82ec2-123">레코드가 버퍼링 되 면 15 초 마다 이벤트 허브에 또는 버퍼가 256 KB의 메시지를 받을 때마다 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-123">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ec2-124">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="82ec2-124">-LoggerId</span></span>
<span data-ttu-id="82ec2-125">로 거에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-125">Specifies an ID for the logger.</span></span>
<span data-ttu-id="82ec2-126">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="82ec2-127">-이름</span><span class="sxs-lookup"><span data-stu-id="82ec2-127">-Name</span></span>
<span data-ttu-id="82ec2-128">Azure 클래식 포털에서 이벤트 허브의 엔터티 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-128">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="82ec2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ec2-129">CommonParameters</span></span>
<span data-ttu-id="82ec2-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ec2-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ec2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ec2-132">입력</span><span class="sxs-lookup"><span data-stu-id="82ec2-132">INPUTS</span></span>

### <span data-ttu-id="82ec2-133">않아야</span><span class="sxs-lookup"><span data-stu-id="82ec2-133">None</span></span>
<span data-ttu-id="82ec2-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82ec2-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82ec2-135">출력</span><span class="sxs-lookup"><span data-stu-id="82ec2-135">OUTPUTS</span></span>

### <span data-ttu-id="82ec2-136">ApiManagement. ServiceManagement. \ PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="82ec2-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="82ec2-137">상속자</span><span class="sxs-lookup"><span data-stu-id="82ec2-137">NOTES</span></span>

## <span data-ttu-id="82ec2-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82ec2-138">RELATED LINKS</span></span>

[<span data-ttu-id="82ec2-139">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="82ec2-139">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="82ec2-140">제거-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="82ec2-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="82ec2-141">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="82ec2-141">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


