---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 359b98d19edfdbdd3c1ce8d6ab7286f13cf5dbfa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711650"
---
# <span data-ttu-id="86a44-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86a44-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="86a44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86a44-102">SYNOPSIS</span></span>
<span data-ttu-id="86a44-103">응용 프로그램 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86a44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86a44-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86a44-105">설명은</span><span class="sxs-lookup"><span data-stu-id="86a44-105">DESCRIPTION</span></span>
<span data-ttu-id="86a44-106">**AzureRmApplicationSecurityGroup** cmdlet은 응용 프로그램 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="86a44-107">예제의</span><span class="sxs-lookup"><span data-stu-id="86a44-107">EXAMPLES</span></span>

### <span data-ttu-id="86a44-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="86a44-108">Example 1</span></span>
```
PS C:\> New-AzureRmApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="86a44-109">이 예제에서는 연결이 없는 응용 프로그램 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="86a44-110">생성 된 네트워크 인터페이스의 IP 구성은 그룹에 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="86a44-111">또한 보안 규칙은 그룹을 원본 또는 대상으로 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="86a44-112">변수</span><span class="sxs-lookup"><span data-stu-id="86a44-112">PARAMETERS</span></span>

### <span data-ttu-id="86a44-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86a44-113">-AsJob</span></span>
<span data-ttu-id="86a44-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="86a44-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86a44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a44-115">-DefaultProfile</span></span>
<span data-ttu-id="86a44-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86a44-117">-Force</span><span class="sxs-lookup"><span data-stu-id="86a44-117">-Force</span></span>
<span data-ttu-id="86a44-118">리소스를 덮어쓰려고 하는 경우 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="86a44-119">-위치</span><span class="sxs-lookup"><span data-stu-id="86a44-119">-Location</span></span>
<span data-ttu-id="86a44-120">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-120">The location.</span></span>

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

### <span data-ttu-id="86a44-121">-이름</span><span class="sxs-lookup"><span data-stu-id="86a44-121">-Name</span></span>
<span data-ttu-id="86a44-122">응용 프로그램 보안 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="86a44-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86a44-123">-ResourceGroupName</span></span>
<span data-ttu-id="86a44-124">응용 프로그램 보안 그룹의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="86a44-125">태그</span><span class="sxs-lookup"><span data-stu-id="86a44-125">-Tag</span></span>
<span data-ttu-id="86a44-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="86a44-127">-확인</span><span class="sxs-lookup"><span data-stu-id="86a44-127">-Confirm</span></span>
<span data-ttu-id="86a44-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86a44-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86a44-129">-WhatIf</span></span>
<span data-ttu-id="86a44-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86a44-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86a44-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a44-132">CommonParameters</span></span>
<span data-ttu-id="86a44-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86a44-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a44-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86a44-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a44-135">입력</span><span class="sxs-lookup"><span data-stu-id="86a44-135">INPUTS</span></span>

### <span data-ttu-id="86a44-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="86a44-136">System.String</span></span>

### <span data-ttu-id="86a44-137">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="86a44-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="86a44-138">출력</span><span class="sxs-lookup"><span data-stu-id="86a44-138">OUTPUTS</span></span>

### <span data-ttu-id="86a44-139">Microsoft. \* PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86a44-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="86a44-140">상속자</span><span class="sxs-lookup"><span data-stu-id="86a44-140">NOTES</span></span>

## <span data-ttu-id="86a44-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86a44-141">RELATED LINKS</span></span>

[<span data-ttu-id="86a44-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86a44-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="86a44-143">제거-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86a44-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="86a44-144">새로운 AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86a44-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="86a44-145">추가-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86a44-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="86a44-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86a44-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="86a44-147">새로운 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="86a44-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="86a44-148">추가-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="86a44-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="86a44-149">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="86a44-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
