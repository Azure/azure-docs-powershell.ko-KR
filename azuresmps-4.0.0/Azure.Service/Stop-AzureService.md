---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 939A28A4-394A-4447-9EFA-8F2876D04DCD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b140c2c0efac81e361e2bab510cfeaf6210ef884
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045807"
---
# <span data-ttu-id="fa9de-101">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="fa9de-101">Stop-AzureService</span></span>

## <span data-ttu-id="fa9de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa9de-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9de-103">현재 호스팅된 서비스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-103">Stops the current hosted service.</span></span>

## <span data-ttu-id="fa9de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa9de-104">SYNTAX</span></span>

```
Stop-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa9de-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fa9de-105">DESCRIPTION</span></span>
<span data-ttu-id="fa9de-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fa9de-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fa9de-108">이 ( **가) azureservice** Cmdlet은 Windows Azure의 지정 된 슬롯에서 현재 호스팅된 서비스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-108">The **Stop-AzureService** cmdlet stops the current hosted service in the specified slot in Windows Azure.</span></span>
<span data-ttu-id="fa9de-109">슬롯을 지정 하지 않으면 cmdlet이 프로덕션 슬롯에서 서비스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-109">If no slot is specified, the cmdlet stops the service in the Production slot.</span></span>

## <span data-ttu-id="fa9de-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fa9de-110">EXAMPLES</span></span>

## <span data-ttu-id="fa9de-111">변수</span><span class="sxs-lookup"><span data-stu-id="fa9de-111">PARAMETERS</span></span>

### <span data-ttu-id="fa9de-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa9de-112">-PassThru</span></span>
<span data-ttu-id="fa9de-113">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa9de-114">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa9de-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="fa9de-115">-Profile</span></span>
<span data-ttu-id="fa9de-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fa9de-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa9de-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fa9de-118">-ServiceName</span></span>
<span data-ttu-id="fa9de-119">중지할 호스팅된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-119">Specifies the name of the hosted service to stop.</span></span>
<span data-ttu-id="fa9de-120">이름을 지정 하지 않으면 cmdlet에서 현재 호스팅된 서비스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-120">If no name is specified, the cmdlet stops the current hosted service.</span></span>

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

### <span data-ttu-id="fa9de-121">-슬롯</span><span class="sxs-lookup"><span data-stu-id="fa9de-121">-Slot</span></span>
<span data-ttu-id="fa9de-122">서비스가 호스팅되는 슬롯 (스테이징 또는 프로덕션)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-122">Specifies the slot where the service is hosted, either Staging or Production.</span></span>
<span data-ttu-id="fa9de-123">슬롯을 지정 하지 않으면 프로덕션으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-123">If no slot is specified,  Production is assumed.</span></span>

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

### <span data-ttu-id="fa9de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9de-124">CommonParameters</span></span>
<span data-ttu-id="fa9de-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9de-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa9de-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9de-127">입력</span><span class="sxs-lookup"><span data-stu-id="fa9de-127">INPUTS</span></span>

## <span data-ttu-id="fa9de-128">출력</span><span class="sxs-lookup"><span data-stu-id="fa9de-128">OUTPUTS</span></span>

## <span data-ttu-id="fa9de-129">상속자</span><span class="sxs-lookup"><span data-stu-id="fa9de-129">NOTES</span></span>

## <span data-ttu-id="fa9de-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa9de-130">RELATED LINKS</span></span>

[<span data-ttu-id="fa9de-131">-AzureService 제거</span><span class="sxs-lookup"><span data-stu-id="fa9de-131">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="fa9de-132">시작-AzureService</span><span class="sxs-lookup"><span data-stu-id="fa9de-132">Start-AzureService</span></span>](./Start-AzureService.md)


