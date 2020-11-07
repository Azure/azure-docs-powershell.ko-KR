---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: cec41bda56da33f22def6c44752effb3d705b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702646"
---
# <span data-ttu-id="7737e-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="7737e-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="7737e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7737e-102">SYNOPSIS</span></span>
<span data-ttu-id="7737e-103">지정 된 이벤트 허브 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7737e-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7737e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7737e-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7737e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7737e-105">DESCRIPTION</span></span>
<span data-ttu-id="7737e-106">Remove-AzureRmEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7737e-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="7737e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7737e-107">EXAMPLES</span></span>

### <span data-ttu-id="7737e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7737e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="7737e-109">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 허브 네임 스페이스 MyNamespaceName를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="7737e-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7737e-110">변수</span><span class="sxs-lookup"><span data-stu-id="7737e-110">PARAMETERS</span></span>

### <span data-ttu-id="7737e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7737e-111">-DefaultProfile</span></span>
<span data-ttu-id="7737e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7737e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7737e-113">-이름</span><span class="sxs-lookup"><span data-stu-id="7737e-113">-Name</span></span>
<span data-ttu-id="7737e-114">EventHub 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="7737e-114">EventHub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7737e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7737e-115">-ResourceGroupName</span></span>
<span data-ttu-id="7737e-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7737e-116">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7737e-117">-확인</span><span class="sxs-lookup"><span data-stu-id="7737e-117">-Confirm</span></span>
<span data-ttu-id="7737e-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7737e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7737e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7737e-119">-WhatIf</span></span>
<span data-ttu-id="7737e-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7737e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7737e-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7737e-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7737e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7737e-122">CommonParameters</span></span>
<span data-ttu-id="7737e-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7737e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7737e-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7737e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7737e-125">입력</span><span class="sxs-lookup"><span data-stu-id="7737e-125">INPUTS</span></span>

### <span data-ttu-id="7737e-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7737e-126">System.String</span></span>


## <span data-ttu-id="7737e-127">출력</span><span class="sxs-lookup"><span data-stu-id="7737e-127">OUTPUTS</span></span>

### <span data-ttu-id="7737e-128">System. 개체</span><span class="sxs-lookup"><span data-stu-id="7737e-128">System.Object</span></span>

## <span data-ttu-id="7737e-129">상속자</span><span class="sxs-lookup"><span data-stu-id="7737e-129">NOTES</span></span>

## <span data-ttu-id="7737e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7737e-130">RELATED LINKS</span></span>
