---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: eb42dc22f972928405821e8468e5610fa9c4514f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871929"
---
# <span data-ttu-id="e9832-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="e9832-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="e9832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9832-102">SYNOPSIS</span></span>
<span data-ttu-id="e9832-103">기존 릴레이 네임 스페이스에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9832-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="e9832-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9832-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9832-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e9832-105">DESCRIPTION</span></span>
<span data-ttu-id="e9832-106">**Set-AzRelayNamespace** cmdlet은 리소스 그룹 내의 지정 된 릴레이 네임 스페이스에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9832-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="e9832-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e9832-107">EXAMPLES</span></span>

### <span data-ttu-id="e9832-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9832-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="e9832-109">새 설명으로 릴레이 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9832-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="e9832-110">변수</span><span class="sxs-lookup"><span data-stu-id="e9832-110">PARAMETERS</span></span>

### <span data-ttu-id="e9832-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9832-111">-DefaultProfile</span></span>
<span data-ttu-id="e9832-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9832-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9832-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9832-113">-InputObject</span></span>
<span data-ttu-id="e9832-114">Relay 네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="e9832-114">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9832-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e9832-115">-Name</span></span>
<span data-ttu-id="e9832-116">릴레이 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9832-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="e9832-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9832-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9832-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9832-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="e9832-119">태그</span><span class="sxs-lookup"><span data-stu-id="e9832-119">-Tag</span></span>
<span data-ttu-id="e9832-120">리소스 태그를 나타내는 Hashtables입니다.</span><span class="sxs-lookup"><span data-stu-id="e9832-120">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9832-121">-확인</span><span class="sxs-lookup"><span data-stu-id="e9832-121">-Confirm</span></span>
<span data-ttu-id="e9832-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9832-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9832-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9832-123">-WhatIf</span></span>
<span data-ttu-id="e9832-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9832-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9832-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9832-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9832-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9832-126">CommonParameters</span></span>
<span data-ttu-id="e9832-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9832-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9832-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9832-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9832-129">입력</span><span class="sxs-lookup"><span data-stu-id="e9832-129">INPUTS</span></span>

### <span data-ttu-id="e9832-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e9832-130">System.String</span></span>

### <span data-ttu-id="e9832-131">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="e9832-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e9832-132">RelayNamespaceAttirbutesUpdateParameter에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="e9832-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="e9832-133">출력</span><span class="sxs-lookup"><span data-stu-id="e9832-133">OUTPUTS</span></span>

### <span data-ttu-id="e9832-134">PSRelayNamespaceAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="e9832-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="e9832-135">상속자</span><span class="sxs-lookup"><span data-stu-id="e9832-135">NOTES</span></span>

## <span data-ttu-id="e9832-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9832-136">RELATED LINKS</span></span>
