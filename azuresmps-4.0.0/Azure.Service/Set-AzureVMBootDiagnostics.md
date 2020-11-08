---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 846B9EB8-8EC2-4BDA-90EF-59098696F460
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c4e1dedb02286ceaab182e0912198c23ec03ee5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045793"
---
# <span data-ttu-id="9a09e-101">Set-AzureVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9a09e-101">Set-AzureVMBootDiagnostics</span></span>

## <span data-ttu-id="9a09e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a09e-102">SYNOPSIS</span></span>

## <span data-ttu-id="9a09e-103">구문과</span><span class="sxs-lookup"><span data-stu-id="9a09e-103">SYNTAX</span></span>

### <span data-ttu-id="9a09e-104">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9a09e-104">EnableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Enable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9a09e-105">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9a09e-105">DisableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9a09e-106">설명은</span><span class="sxs-lookup"><span data-stu-id="9a09e-106">DESCRIPTION</span></span>

## <span data-ttu-id="9a09e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9a09e-107">EXAMPLES</span></span>

### <span data-ttu-id="9a09e-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="9a09e-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="9a09e-109">변수</span><span class="sxs-lookup"><span data-stu-id="9a09e-109">PARAMETERS</span></span>

### <span data-ttu-id="9a09e-110">-Disable</span><span class="sxs-lookup"><span data-stu-id="9a09e-110">-Disable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a09e-111">-사용</span><span class="sxs-lookup"><span data-stu-id="9a09e-111">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a09e-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9a09e-112">-InformationAction</span></span>
<span data-ttu-id="9a09e-113">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a09e-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9a09e-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9a09e-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a09e-115">하기로</span><span class="sxs-lookup"><span data-stu-id="9a09e-115">Continue</span></span>
- <span data-ttu-id="9a09e-116">숨기기</span><span class="sxs-lookup"><span data-stu-id="9a09e-116">Ignore</span></span>
- <span data-ttu-id="9a09e-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="9a09e-117">Inquire</span></span>
- <span data-ttu-id="9a09e-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9a09e-118">SilentlyContinue</span></span>
- <span data-ttu-id="9a09e-119">중지가</span><span class="sxs-lookup"><span data-stu-id="9a09e-119">Stop</span></span>
- <span data-ttu-id="9a09e-120">대기</span><span class="sxs-lookup"><span data-stu-id="9a09e-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a09e-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9a09e-121">-InformationVariable</span></span>
<span data-ttu-id="9a09e-122">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a09e-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a09e-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="9a09e-123">-Profile</span></span>
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

### <span data-ttu-id="9a09e-124">-VM</span><span class="sxs-lookup"><span data-stu-id="9a09e-124">-VM</span></span>
```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a09e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a09e-125">CommonParameters</span></span>
<span data-ttu-id="9a09e-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a09e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a09e-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a09e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a09e-128">입력</span><span class="sxs-lookup"><span data-stu-id="9a09e-128">INPUTS</span></span>

## <span data-ttu-id="9a09e-129">출력</span><span class="sxs-lookup"><span data-stu-id="9a09e-129">OUTPUTS</span></span>

## <span data-ttu-id="9a09e-130">상속자</span><span class="sxs-lookup"><span data-stu-id="9a09e-130">NOTES</span></span>

## <span data-ttu-id="9a09e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a09e-131">RELATED LINKS</span></span>

