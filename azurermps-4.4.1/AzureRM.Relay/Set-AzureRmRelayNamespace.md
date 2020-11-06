---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: c243f31ee549443ad959bde13abc9ff3b68c1560
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529174"
---
# <span data-ttu-id="c4df7-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="c4df7-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="c4df7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4df7-102">SYNOPSIS</span></span>
<span data-ttu-id="c4df7-103">기존 릴레이 네임 스페이스에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4df7-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4df7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4df7-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4df7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c4df7-105">DESCRIPTION</span></span>
<span data-ttu-id="c4df7-106">**Set-AzureRmRelayNamespace** cmdlet은 리소스 그룹 내의 지정 된 릴레이 네임 스페이스에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4df7-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="c4df7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c4df7-107">EXAMPLES</span></span>

### <span data-ttu-id="c4df7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4df7-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="c4df7-109">새 설명으로 릴레이 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4df7-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="c4df7-110">변수</span><span class="sxs-lookup"><span data-stu-id="c4df7-110">PARAMETERS</span></span>

### <span data-ttu-id="c4df7-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4df7-111">-ResourceGroupName</span></span>
<span data-ttu-id="c4df7-112">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4df7-112">Resource Group Name.</span></span>

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

### <span data-ttu-id="c4df7-113">태그</span><span class="sxs-lookup"><span data-stu-id="c4df7-113">-Tag</span></span>
<span data-ttu-id="c4df7-114">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c4df7-114">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c4df7-115">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="c4df7-115">For example:</span></span>

<span data-ttu-id="c4df7-116">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c4df7-116">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c4df7-117">-확인</span><span class="sxs-lookup"><span data-stu-id="c4df7-117">-Confirm</span></span>
<span data-ttu-id="c4df7-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4df7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4df7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4df7-119">-WhatIf</span></span>
<span data-ttu-id="c4df7-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4df7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4df7-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4df7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4df7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4df7-122">-DefaultProfile</span></span>
<span data-ttu-id="c4df7-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4df7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4df7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4df7-124">-InputObject</span></span>
<span data-ttu-id="c4df7-125">Relay 네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="c4df7-125">Relay Namespace object.</span></span>

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

### <span data-ttu-id="c4df7-126">-이름</span><span class="sxs-lookup"><span data-stu-id="c4df7-126">-Name</span></span>
<span data-ttu-id="c4df7-127">릴레이 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4df7-127">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="c4df7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4df7-128">CommonParameters</span></span>
<span data-ttu-id="c4df7-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4df7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4df7-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4df7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4df7-131">입력</span><span class="sxs-lookup"><span data-stu-id="c4df7-131">INPUTS</span></span>

### <span data-ttu-id="c4df7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4df7-132">-ResourceGroupName</span></span>
 <span data-ttu-id="c4df7-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c4df7-133">System.String</span></span>

### <span data-ttu-id="c4df7-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c4df7-134">-NamespaceName</span></span>
 <span data-ttu-id="c4df7-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c4df7-135">System.String</span></span>

### <span data-ttu-id="c4df7-136">-위치</span><span class="sxs-lookup"><span data-stu-id="c4df7-136">-Location</span></span>
 <span data-ttu-id="c4df7-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c4df7-137">System.String</span></span>

### <span data-ttu-id="c4df7-138">태그</span><span class="sxs-lookup"><span data-stu-id="c4df7-138">-Tag</span></span>
 <span data-ttu-id="c4df7-139">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="c4df7-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c4df7-140">출력</span><span class="sxs-lookup"><span data-stu-id="c4df7-140">OUTPUTS</span></span>

### <span data-ttu-id="c4df7-141">RelayNamespaceAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="c4df7-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="c4df7-142">상속자</span><span class="sxs-lookup"><span data-stu-id="c4df7-142">NOTES</span></span>

## <span data-ttu-id="c4df7-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4df7-143">RELATED LINKS</span></span>

