---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 551428a1c5d1737d32aeddf2dd5653586d1dbfbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965083"
---
# <span data-ttu-id="abe6c-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="abe6c-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="abe6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abe6c-102">SYNOPSIS</span></span>
<span data-ttu-id="abe6c-103">매개 변수에 의해 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="abe6c-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="abe6c-104">구문</span><span class="sxs-lookup"><span data-stu-id="abe6c-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="abe6c-105">설명</span><span class="sxs-lookup"><span data-stu-id="abe6c-105">DESCRIPTION</span></span>
<span data-ttu-id="abe6c-106">매개 변수에 의해 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="abe6c-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="abe6c-107">예제</span><span class="sxs-lookup"><span data-stu-id="abe6c-107">EXAMPLES</span></span>

### <span data-ttu-id="abe6c-108">예제 1: Azure에 BotService 게시</span><span class="sxs-lookup"><span data-stu-id="abe6c-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="abe6c-109">코드로 Azure에 BotService 게시</span><span class="sxs-lookup"><span data-stu-id="abe6c-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="abe6c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="abe6c-110">PARAMETERS</span></span>

### <span data-ttu-id="abe6c-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="abe6c-111">-CodeDir</span></span>
<span data-ttu-id="abe6c-112">이 매개 변수는 ZIP의 경로를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="abe6c-112">This parameter defines the Path of the ZIP</span></span>

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

### <span data-ttu-id="abe6c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="abe6c-113">-Name</span></span>
<span data-ttu-id="abe6c-114">이 매개 변수는 봇의 이름을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="abe6c-114">This parameter defines the name of the bot.</span></span>

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

### <span data-ttu-id="abe6c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abe6c-115">-ResourceGroupName</span></span>
<span data-ttu-id="abe6c-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="abe6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abe6c-117">-확인</span><span class="sxs-lookup"><span data-stu-id="abe6c-117">-Confirm</span></span>
<span data-ttu-id="abe6c-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="abe6c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abe6c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abe6c-119">-WhatIf</span></span>
<span data-ttu-id="abe6c-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="abe6c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abe6c-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abe6c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abe6c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe6c-122">CommonParameters</span></span>
<span data-ttu-id="abe6c-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="abe6c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe6c-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abe6c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe6c-125">입력</span><span class="sxs-lookup"><span data-stu-id="abe6c-125">INPUTS</span></span>

## <span data-ttu-id="abe6c-126">출력</span><span class="sxs-lookup"><span data-stu-id="abe6c-126">OUTPUTS</span></span>

## <span data-ttu-id="abe6c-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="abe6c-127">NOTES</span></span>

<span data-ttu-id="abe6c-128">별칭</span><span class="sxs-lookup"><span data-stu-id="abe6c-128">ALIASES</span></span>

## <span data-ttu-id="abe6c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abe6c-129">RELATED LINKS</span></span>

