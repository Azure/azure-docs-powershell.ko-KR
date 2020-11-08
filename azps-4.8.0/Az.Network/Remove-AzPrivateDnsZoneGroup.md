---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203904"
---
# <span data-ttu-id="95c49-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="95c49-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="95c49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95c49-102">SYNOPSIS</span></span>
<span data-ttu-id="95c49-103">DNS 영역 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95c49-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="95c49-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95c49-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95c49-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95c49-105">DESCRIPTION</span></span>
<span data-ttu-id="95c49-106">**제거-AzPrivateDnsZoneGroup** CMDLET은 DNS 영역 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95c49-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="95c49-107">예제의</span><span class="sxs-lookup"><span data-stu-id="95c49-107">EXAMPLES</span></span>

### <span data-ttu-id="95c49-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="95c49-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="95c49-109">위 예제에서는 끝점 테스트-pr-끝점에서 이름이 dnsgroup1 인 DNS 영역에 대해 정리 합니다.</span><span class="sxs-lookup"><span data-stu-id="95c49-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="95c49-110">변수</span><span class="sxs-lookup"><span data-stu-id="95c49-110">PARAMETERS</span></span>

### <span data-ttu-id="95c49-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95c49-111">-AsJob</span></span>
<span data-ttu-id="95c49-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="95c49-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95c49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c49-113">-DefaultProfile</span></span>
<span data-ttu-id="95c49-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95c49-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95c49-115">-Force</span><span class="sxs-lookup"><span data-stu-id="95c49-115">-Force</span></span>
<span data-ttu-id="95c49-116">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="95c49-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="95c49-117">-이름</span><span class="sxs-lookup"><span data-stu-id="95c49-117">-Name</span></span>
<span data-ttu-id="95c49-118">개인 dns 영역 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95c49-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95c49-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95c49-119">-PassThru</span></span>
<span data-ttu-id="95c49-120">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="95c49-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="95c49-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="95c49-121">-PrivateEndpointName</span></span>
<span data-ttu-id="95c49-122">개인 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95c49-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="95c49-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95c49-123">-ResourceGroupName</span></span>
<span data-ttu-id="95c49-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95c49-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="95c49-125">-확인</span><span class="sxs-lookup"><span data-stu-id="95c49-125">-Confirm</span></span>
<span data-ttu-id="95c49-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95c49-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95c49-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95c49-127">-WhatIf</span></span>
<span data-ttu-id="95c49-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="95c49-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95c49-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95c49-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95c49-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c49-130">CommonParameters</span></span>
<span data-ttu-id="95c49-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95c49-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c49-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95c49-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c49-133">입력</span><span class="sxs-lookup"><span data-stu-id="95c49-133">INPUTS</span></span>

### <span data-ttu-id="95c49-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="95c49-134">System.String</span></span>

## <span data-ttu-id="95c49-135">출력</span><span class="sxs-lookup"><span data-stu-id="95c49-135">OUTPUTS</span></span>

### <span data-ttu-id="95c49-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="95c49-136">System.Boolean</span></span>

## <span data-ttu-id="95c49-137">상속자</span><span class="sxs-lookup"><span data-stu-id="95c49-137">NOTES</span></span>

## <span data-ttu-id="95c49-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95c49-138">RELATED LINKS</span></span>
