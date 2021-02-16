---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200844"
---
# <span data-ttu-id="0d3fc-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="0d3fc-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="0d3fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="0d3fc-103">매개 변수로 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="0d3fc-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d3fc-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0d3fc-105">설명</span><span class="sxs-lookup"><span data-stu-id="0d3fc-105">DESCRIPTION</span></span>
<span data-ttu-id="0d3fc-106">매개 변수로 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="0d3fc-107">예제</span><span class="sxs-lookup"><span data-stu-id="0d3fc-107">EXAMPLES</span></span>

### <span data-ttu-id="0d3fc-108">예제 1: Azure에 BotService 게시</span><span class="sxs-lookup"><span data-stu-id="0d3fc-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="0d3fc-109">코드로 Azure에 BotService 게시</span><span class="sxs-lookup"><span data-stu-id="0d3fc-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="0d3fc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d3fc-110">PARAMETERS</span></span>

### <span data-ttu-id="0d3fc-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="0d3fc-111">-CodeDir</span></span>
<span data-ttu-id="0d3fc-112">이 매개 변수는 ZIP의 경로를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-112">This parameter defines the Path of the ZIP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d3fc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0d3fc-113">-Name</span></span>
<span data-ttu-id="0d3fc-114">이 매개 변수는 봇의 이름을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-114">This parameter defines the name of the bot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d3fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d3fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="0d3fc-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d3fc-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d3fc-117">-Confirm</span></span>
<span data-ttu-id="0d3fc-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d3fc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d3fc-119">-WhatIf</span></span>
<span data-ttu-id="0d3fc-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0d3fc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d3fc-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d3fc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d3fc-122">CommonParameters</span></span>
<span data-ttu-id="0d3fc-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d3fc-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0d3fc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d3fc-125">입력</span><span class="sxs-lookup"><span data-stu-id="0d3fc-125">INPUTS</span></span>

## <span data-ttu-id="0d3fc-126">출력</span><span class="sxs-lookup"><span data-stu-id="0d3fc-126">OUTPUTS</span></span>

## <span data-ttu-id="0d3fc-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d3fc-127">NOTES</span></span>

<span data-ttu-id="0d3fc-128">별칭</span><span class="sxs-lookup"><span data-stu-id="0d3fc-128">ALIASES</span></span>

## <span data-ttu-id="0d3fc-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d3fc-129">RELATED LINKS</span></span>

