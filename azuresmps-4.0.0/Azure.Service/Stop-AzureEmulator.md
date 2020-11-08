---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 43E2C42E-16A3-426E-A7C4-33942F06F908
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd94462eb89cff6b4cec97f05911e27dbb05c920
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045766"
---
# <span data-ttu-id="d64a9-101">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="d64a9-101">Stop-AzureEmulator</span></span>

## <span data-ttu-id="d64a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d64a9-102">SYNOPSIS</span></span>
<span data-ttu-id="d64a9-103">계산 에뮬레이터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d64a9-103">Stops the compute emulator.</span></span>

## <span data-ttu-id="d64a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d64a9-104">SYNTAX</span></span>

```
Stop-AzureEmulator [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d64a9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d64a9-105">DESCRIPTION</span></span>
<span data-ttu-id="d64a9-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d64a9-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d64a9-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d64a9-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d64a9-108">**-Azureemulator** Cmdlet은 Azure 계산 에뮬레이터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d64a9-108">The **Stop-AzureEmulator** cmdlet stops the Azure compute emulator.</span></span>
<span data-ttu-id="d64a9-109">에뮬레이터에서 현재 실행 중인 서비스는 모두 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d64a9-109">Any services currently running in the emulator are removed.</span></span>

## <span data-ttu-id="d64a9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d64a9-110">EXAMPLES</span></span>

## <span data-ttu-id="d64a9-111">변수</span><span class="sxs-lookup"><span data-stu-id="d64a9-111">PARAMETERS</span></span>

### <span data-ttu-id="d64a9-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d64a9-112">-PassThru</span></span>
<span data-ttu-id="d64a9-113">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d64a9-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d64a9-114">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d64a9-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d64a9-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="d64a9-115">-Profile</span></span>
<span data-ttu-id="d64a9-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d64a9-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d64a9-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d64a9-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d64a9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64a9-118">CommonParameters</span></span>
<span data-ttu-id="d64a9-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d64a9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64a9-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d64a9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64a9-121">입력</span><span class="sxs-lookup"><span data-stu-id="d64a9-121">INPUTS</span></span>

## <span data-ttu-id="d64a9-122">출력</span><span class="sxs-lookup"><span data-stu-id="d64a9-122">OUTPUTS</span></span>

## <span data-ttu-id="d64a9-123">상속자</span><span class="sxs-lookup"><span data-stu-id="d64a9-123">NOTES</span></span>

## <span data-ttu-id="d64a9-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d64a9-124">RELATED LINKS</span></span>

[<span data-ttu-id="d64a9-125">시작-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="d64a9-125">Start-AzureEmulator</span></span>](./Start-AzureEmulator.md)


