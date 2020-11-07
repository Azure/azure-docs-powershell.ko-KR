---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: ac6327176c587bcb221a5ebddbb12ae9adeffbf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711029"
---
# <span data-ttu-id="b1e3d-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="b1e3d-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="b1e3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e3d-103">지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1e3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1e3d-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1e3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1e3d-105">DESCRIPTION</span></span>
<span data-ttu-id="b1e3d-106">**AzureRmRelayNamespace** cmdlet은 지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="b1e3d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b1e3d-107">EXAMPLES</span></span>

### <span data-ttu-id="b1e3d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b1e3d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="b1e3d-109">지정 된 리소스 그룹에서 릴레이 네임 스페이스를 제거 `TestNameSpace-Relay1` `Default-ServiceBus-WestUS` 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="b1e3d-110">변수</span><span class="sxs-lookup"><span data-stu-id="b1e3d-110">PARAMETERS</span></span>

### <span data-ttu-id="b1e3d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1e3d-111">-DefaultProfile</span></span>
<span data-ttu-id="b1e3d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1e3d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="b1e3d-113">-Name</span></span>
<span data-ttu-id="b1e3d-114">릴레이 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="b1e3d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1e3d-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1e3d-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="b1e3d-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b1e3d-117">-Confirm</span></span>
<span data-ttu-id="b1e3d-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1e3d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1e3d-119">-WhatIf</span></span>
<span data-ttu-id="b1e3d-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1e3d-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1e3d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e3d-122">CommonParameters</span></span>
<span data-ttu-id="b1e3d-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b1e3d-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1e3d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e3d-125">입력</span><span class="sxs-lookup"><span data-stu-id="b1e3d-125">INPUTS</span></span>

### <span data-ttu-id="b1e3d-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b1e3d-126">System.String</span></span>


## <span data-ttu-id="b1e3d-127">출력</span><span class="sxs-lookup"><span data-stu-id="b1e3d-127">OUTPUTS</span></span>

### <span data-ttu-id="b1e3d-128">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="b1e3d-128">System.Void</span></span>


## <span data-ttu-id="b1e3d-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b1e3d-129">NOTES</span></span>

## <span data-ttu-id="b1e3d-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1e3d-130">RELATED LINKS</span></span>
