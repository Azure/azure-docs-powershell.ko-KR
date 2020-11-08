---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046031"
---
# <span data-ttu-id="ffcda-101">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="ffcda-101">Start-AzureEmulator</span></span>

## <span data-ttu-id="ffcda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffcda-102">SYNOPSIS</span></span>
<span data-ttu-id="ffcda-103">계산 및 저장소 에뮬레이터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-103">Starts the compute and storage emulators.</span></span>

## <span data-ttu-id="ffcda-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ffcda-104">SYNTAX</span></span>

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ffcda-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ffcda-105">DESCRIPTION</span></span>
<span data-ttu-id="ffcda-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ffcda-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ffcda-108">**시작 AzureEmulator** cmdlet은 계산 및 저장소 에뮬레이터를 모두 시작 하 고 계산 에뮬레이터에서 현재 서비스를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-108">The **Start-AzureEmulator** cmdlet starts both the compute and storage emulators and hosts the current service in the compute emulator.</span></span>

## <span data-ttu-id="ffcda-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ffcda-109">EXAMPLES</span></span>

### <span data-ttu-id="ffcda-110">예제 1: 에뮬레이터 시작 및 브라우저 시작</span><span class="sxs-lookup"><span data-stu-id="ffcda-110">Example 1: Start the emulator and launch a browser</span></span>
```
PS C:\> Start-AzureEmulator -L
```

<span data-ttu-id="ffcda-111">이 예제에서는 Azure 에뮬레이터에서 서비스를 실행 하 고 에뮬레이트된 서비스에서 새 브라우저 창을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-111">This example runs the service in the Azure emulator and launches a new browser window on the emulated service.</span></span>

## <span data-ttu-id="ffcda-112">변수</span><span class="sxs-lookup"><span data-stu-id="ffcda-112">PARAMETERS</span></span>

### <span data-ttu-id="ffcda-113">-시작</span><span class="sxs-lookup"><span data-stu-id="ffcda-113">-Launch</span></span>
<span data-ttu-id="ffcda-114">에뮬레이터에서 서비스를 호스팅한 후 새 브라우저 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-114">Opens a new browser window on the service after hosting it in the emulator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcda-115">-모드</span><span class="sxs-lookup"><span data-stu-id="ffcda-115">-Mode</span></span>
<span data-ttu-id="ffcda-116">에뮬레이터 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-116">Specifies the emulator mode.</span></span>
<span data-ttu-id="ffcda-117">유효한 값은 Full 및 Express입니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-117">Valid values are: Full and Express.</span></span>
<span data-ttu-id="ffcda-118">기본 값은 Express입니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-118">The default value is Express.</span></span>

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcda-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="ffcda-119">-Profile</span></span>
<span data-ttu-id="ffcda-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ffcda-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ffcda-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffcda-122">CommonParameters</span></span>
<span data-ttu-id="ffcda-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffcda-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffcda-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffcda-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffcda-125">입력</span><span class="sxs-lookup"><span data-stu-id="ffcda-125">INPUTS</span></span>

## <span data-ttu-id="ffcda-126">출력</span><span class="sxs-lookup"><span data-stu-id="ffcda-126">OUTPUTS</span></span>

## <span data-ttu-id="ffcda-127">상속자</span><span class="sxs-lookup"><span data-stu-id="ffcda-127">NOTES</span></span>

## <span data-ttu-id="ffcda-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffcda-128">RELATED LINKS</span></span>

[<span data-ttu-id="ffcda-129">새-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="ffcda-129">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="ffcda-130">게시-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="ffcda-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="ffcda-131">정지-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="ffcda-131">Stop-AzureEmulator</span></span>](./Stop-AzureEmulator.md)


