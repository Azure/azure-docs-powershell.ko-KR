---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 65540c331074b5c140bafe9e87d625dfaec2f252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538119"
---
# <span data-ttu-id="b0a05-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b0a05-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="b0a05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a05-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0a05-103">구문과</span><span class="sxs-lookup"><span data-stu-id="b0a05-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0a05-104">설명은</span><span class="sxs-lookup"><span data-stu-id="b0a05-104">DESCRIPTION</span></span>

## <span data-ttu-id="b0a05-105">예제의</span><span class="sxs-lookup"><span data-stu-id="b0a05-105">EXAMPLES</span></span>

## <span data-ttu-id="b0a05-106">변수</span><span class="sxs-lookup"><span data-stu-id="b0a05-106">PARAMETERS</span></span>

### <span data-ttu-id="b0a05-107">-Force</span><span class="sxs-lookup"><span data-stu-id="b0a05-107">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a05-108">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="b0a05-108">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a05-109">-이름</span><span class="sxs-lookup"><span data-stu-id="b0a05-109">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a05-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a05-110">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a05-111">-확인</span><span class="sxs-lookup"><span data-stu-id="b0a05-111">-Confirm</span></span>
<span data-ttu-id="b0a05-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a05-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0a05-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0a05-113">-WhatIf</span></span>
<span data-ttu-id="b0a05-114">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0a05-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0a05-115">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a05-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0a05-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a05-116">-DefaultProfile</span></span>
<span data-ttu-id="b0a05-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a05-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0a05-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a05-118">CommonParameters</span></span>
<span data-ttu-id="b0a05-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a05-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a05-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0a05-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a05-121">입력</span><span class="sxs-lookup"><span data-stu-id="b0a05-121">INPUTS</span></span>

## <span data-ttu-id="b0a05-122">출력</span><span class="sxs-lookup"><span data-stu-id="b0a05-122">OUTPUTS</span></span>

### <span data-ttu-id="b0a05-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b0a05-123">System.String</span></span>

## <span data-ttu-id="b0a05-124">상속자</span><span class="sxs-lookup"><span data-stu-id="b0a05-124">NOTES</span></span>

## <span data-ttu-id="b0a05-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0a05-125">RELATED LINKS</span></span>

[<span data-ttu-id="b0a05-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b0a05-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="b0a05-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b0a05-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


