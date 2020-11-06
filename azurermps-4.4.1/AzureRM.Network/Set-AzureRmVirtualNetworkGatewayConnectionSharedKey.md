---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1c51d58d7732a3f9d07f1beba24a7584b35733b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530757"
---
# <span data-ttu-id="47f63-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="47f63-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="47f63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47f63-102">SYNOPSIS</span></span>
<span data-ttu-id="47f63-103">가상 네트워크 게이트웨이 연결의 공유 키를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f63-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47f63-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47f63-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47f63-105">설명은</span><span class="sxs-lookup"><span data-stu-id="47f63-105">DESCRIPTION</span></span>
<span data-ttu-id="47f63-106">**Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet은 가상 네트워크 게이트웨이 연결의 공유 키를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f63-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="47f63-107">예제의</span><span class="sxs-lookup"><span data-stu-id="47f63-107">EXAMPLES</span></span>

## <span data-ttu-id="47f63-108">변수</span><span class="sxs-lookup"><span data-stu-id="47f63-108">PARAMETERS</span></span>

### <span data-ttu-id="47f63-109">-Force</span><span class="sxs-lookup"><span data-stu-id="47f63-109">-Force</span></span>
<span data-ttu-id="47f63-110">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f63-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="47f63-111">-이름</span><span class="sxs-lookup"><span data-stu-id="47f63-111">-Name</span></span>
<span data-ttu-id="47f63-112">가상 네트워크 게이트웨이 공유 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f63-112">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="47f63-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47f63-113">-ResourceGroupName</span></span>
<span data-ttu-id="47f63-114">가상 네트워크 게이트웨이가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f63-114">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="47f63-115">-값</span><span class="sxs-lookup"><span data-stu-id="47f63-115">-Value</span></span>
<span data-ttu-id="47f63-116">공유 키의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f63-116">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="47f63-117">-확인</span><span class="sxs-lookup"><span data-stu-id="47f63-117">-Confirm</span></span>
<span data-ttu-id="47f63-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f63-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47f63-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47f63-119">-WhatIf</span></span>
<span data-ttu-id="47f63-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="47f63-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47f63-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47f63-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47f63-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f63-122">-DefaultProfile</span></span>
<span data-ttu-id="47f63-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47f63-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47f63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f63-124">CommonParameters</span></span>
<span data-ttu-id="47f63-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f63-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47f63-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f63-127">입력</span><span class="sxs-lookup"><span data-stu-id="47f63-127">INPUTS</span></span>

## <span data-ttu-id="47f63-128">출력</span><span class="sxs-lookup"><span data-stu-id="47f63-128">OUTPUTS</span></span>

### <span data-ttu-id="47f63-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="47f63-129">System.String</span></span>

## <span data-ttu-id="47f63-130">상속자</span><span class="sxs-lookup"><span data-stu-id="47f63-130">NOTES</span></span>

## <span data-ttu-id="47f63-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47f63-131">RELATED LINKS</span></span>

[<span data-ttu-id="47f63-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="47f63-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="47f63-133">다시 설정-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="47f63-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


