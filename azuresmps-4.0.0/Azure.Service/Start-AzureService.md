---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 821CB3E4-102E-440A-8C92-D1890899A6EE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 64924d579eebb826bc9c36468da1617370f48cf7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046030"
---
# <span data-ttu-id="12e42-101">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="12e42-101">Start-AzureService</span></span>

## <span data-ttu-id="12e42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e42-102">SYNOPSIS</span></span>
<span data-ttu-id="12e42-103">Windows Azure에서 지정 된 호스팅된 서비스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-103">Starts the specified hosted service in Windows Azure.</span></span>

## <span data-ttu-id="12e42-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12e42-104">SYNTAX</span></span>

```
Start-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="12e42-105">설명은</span><span class="sxs-lookup"><span data-stu-id="12e42-105">DESCRIPTION</span></span>
<span data-ttu-id="12e42-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="12e42-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="12e42-108">서비스가 중지 된 상태인 경우 **시작-azureservice** Cmdlet은 Windows Azure에서 지정 된 호스팅된 서비스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-108">The **Start-AzureService** cmdlet starts the specified hosted service in Windows Azure, if the service is in the stopped state.</span></span>
<span data-ttu-id="12e42-109">**게시-AzureServiceProject** cmdlet은 자동으로 서비스 시작을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-109">Note that the **Publish-AzureServiceProject** cmdlet automatically attempts to start the service.</span></span>

## <span data-ttu-id="12e42-110">예제의</span><span class="sxs-lookup"><span data-stu-id="12e42-110">EXAMPLES</span></span>

## <span data-ttu-id="12e42-111">변수</span><span class="sxs-lookup"><span data-stu-id="12e42-111">PARAMETERS</span></span>

### <span data-ttu-id="12e42-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12e42-112">-PassThru</span></span>
<span data-ttu-id="12e42-113">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="12e42-114">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="12e42-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="12e42-115">-Profile</span></span>
<span data-ttu-id="12e42-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="12e42-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12e42-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="12e42-118">-ServiceName</span></span>
<span data-ttu-id="12e42-119">시작할 호스팅된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-119">Specifies the name of the hosted service to start.</span></span>
<span data-ttu-id="12e42-120">이름을 지정 하지 않으면 cmdlet에서 현재 호스팅된 서비스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-120">If no name is specified, the cmdlet starts the current hosted service.</span></span>

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

### <span data-ttu-id="12e42-121">-슬롯</span><span class="sxs-lookup"><span data-stu-id="12e42-121">-Slot</span></span>
<span data-ttu-id="12e42-122">서비스를 시작할 배포 슬롯을 스테이징 또는 프로덕션 중에서 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-122">Specifies the deployment slot in which to start the service, either Staging or Production.</span></span>

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

### <span data-ttu-id="12e42-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e42-123">CommonParameters</span></span>
<span data-ttu-id="12e42-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e42-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e42-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e42-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e42-126">입력</span><span class="sxs-lookup"><span data-stu-id="12e42-126">INPUTS</span></span>

## <span data-ttu-id="12e42-127">출력</span><span class="sxs-lookup"><span data-stu-id="12e42-127">OUTPUTS</span></span>

## <span data-ttu-id="12e42-128">상속자</span><span class="sxs-lookup"><span data-stu-id="12e42-128">NOTES</span></span>

## <span data-ttu-id="12e42-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12e42-129">RELATED LINKS</span></span>

[<span data-ttu-id="12e42-130">-AzureService 제거</span><span class="sxs-lookup"><span data-stu-id="12e42-130">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="12e42-131">시작-AzureService</span><span class="sxs-lookup"><span data-stu-id="12e42-131">Start-AzureService</span></span>](./Start-AzureService.md)

[<span data-ttu-id="12e42-132">정지-AzureService</span><span class="sxs-lookup"><span data-stu-id="12e42-132">Stop-AzureService</span></span>](./Stop-AzureService.md)


