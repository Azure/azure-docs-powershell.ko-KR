---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: a774f388690ab2ee0528e94a2a96addecf1687fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537003"
---
# <span data-ttu-id="33e6e-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="33e6e-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="33e6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="33e6e-103">지정 된 릴레이 네임 스페이스에서 WcfRelay를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e6e-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33e6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33e6e-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33e6e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="33e6e-105">DESCRIPTION</span></span>
<span data-ttu-id="33e6e-106">**Remove-AzureRmWcfRelay** cmdlet은 지정 된 릴레이 네임 스페이스에서 WcfRelay를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e6e-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="33e6e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="33e6e-107">EXAMPLES</span></span>

### <span data-ttu-id="33e6e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="33e6e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="33e6e-109">네임 스페이스에서 WcfRelay를 제거 합니다 `TestWCFRelay1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="33e6e-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="33e6e-110">변수</span><span class="sxs-lookup"><span data-stu-id="33e6e-110">PARAMETERS</span></span>

### <span data-ttu-id="33e6e-111">-Namespace</span><span class="sxs-lookup"><span data-stu-id="33e6e-111">-Namespace</span></span>
<span data-ttu-id="33e6e-112">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33e6e-112">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e6e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e6e-113">-ResourceGroupName</span></span>
<span data-ttu-id="33e6e-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33e6e-114">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e6e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="33e6e-115">-Name</span></span>
<span data-ttu-id="33e6e-116">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33e6e-116">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e6e-117">-확인</span><span class="sxs-lookup"><span data-stu-id="33e6e-117">-Confirm</span></span>
<span data-ttu-id="33e6e-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e6e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33e6e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33e6e-119">-WhatIf</span></span>
<span data-ttu-id="33e6e-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33e6e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33e6e-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33e6e-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33e6e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e6e-122">-DefaultProfile</span></span>
<span data-ttu-id="33e6e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33e6e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33e6e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e6e-124">CommonParameters</span></span>
<span data-ttu-id="33e6e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e6e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e6e-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33e6e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e6e-127">입력</span><span class="sxs-lookup"><span data-stu-id="33e6e-127">INPUTS</span></span>

### <span data-ttu-id="33e6e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e6e-128">-ResourceGroupName</span></span>
 <span data-ttu-id="33e6e-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33e6e-129">System.String</span></span>
 

### <span data-ttu-id="33e6e-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="33e6e-130">-Namespace</span></span>
 <span data-ttu-id="33e6e-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33e6e-131">System.String</span></span>
 

### <span data-ttu-id="33e6e-132">-이름</span><span class="sxs-lookup"><span data-stu-id="33e6e-132">-Name</span></span>
 <span data-ttu-id="33e6e-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33e6e-133">System.String</span></span>

## <span data-ttu-id="33e6e-134">출력</span><span class="sxs-lookup"><span data-stu-id="33e6e-134">OUTPUTS</span></span>

### <span data-ttu-id="33e6e-135">System. 개체</span><span class="sxs-lookup"><span data-stu-id="33e6e-135">System.Object</span></span>

## <span data-ttu-id="33e6e-136">상속자</span><span class="sxs-lookup"><span data-stu-id="33e6e-136">NOTES</span></span>

## <span data-ttu-id="33e6e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33e6e-137">RELATED LINKS</span></span>

