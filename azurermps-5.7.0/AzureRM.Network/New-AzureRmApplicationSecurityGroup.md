---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 82fdec48f2e021e33490f84a05a064fb007ac8d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528035"
---
# <span data-ttu-id="7cb40-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7cb40-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="7cb40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cb40-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb40-103">응용 프로그램 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cb40-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7cb40-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cb40-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7cb40-105">DESCRIPTION</span></span>
<span data-ttu-id="7cb40-106">**AzureRmApplicationSecurityGroup** cmdlet은 응용 프로그램 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="7cb40-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7cb40-107">EXAMPLES</span></span>

### <span data-ttu-id="7cb40-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7cb40-108">Example 1</span></span>
```
PS C:\> New-AzureRmApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="7cb40-109">이 예제에서는 연결이 없는 응용 프로그램 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="7cb40-110">생성 된 네트워크 인터페이스의 IP 구성은 그룹에 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="7cb40-111">또한 보안 규칙은 그룹을 원본 또는 대상으로 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="7cb40-112">변수</span><span class="sxs-lookup"><span data-stu-id="7cb40-112">PARAMETERS</span></span>

### <span data-ttu-id="7cb40-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cb40-113">-AsJob</span></span>
<span data-ttu-id="7cb40-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7cb40-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb40-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb40-115">-DefaultProfile</span></span>
<span data-ttu-id="7cb40-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cb40-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7cb40-117">-Force</span></span>
<span data-ttu-id="7cb40-118">리소스를 덮어쓰려고 하는 경우 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb40-119">-위치</span><span class="sxs-lookup"><span data-stu-id="7cb40-119">-Location</span></span>
<span data-ttu-id="7cb40-120">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb40-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7cb40-121">-Name</span></span>
<span data-ttu-id="7cb40-122">응용 프로그램 보안 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-122">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb40-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb40-123">-ResourceGroupName</span></span>
<span data-ttu-id="7cb40-124">응용 프로그램 보안 그룹의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-124">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb40-125">태그</span><span class="sxs-lookup"><span data-stu-id="7cb40-125">-Tag</span></span>
<span data-ttu-id="7cb40-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb40-127">-확인</span><span class="sxs-lookup"><span data-stu-id="7cb40-127">-Confirm</span></span>
<span data-ttu-id="7cb40-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb40-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb40-129">-WhatIf</span></span>
<span data-ttu-id="7cb40-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb40-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cb40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb40-132">CommonParameters</span></span>
<span data-ttu-id="7cb40-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb40-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cb40-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb40-135">입력</span><span class="sxs-lookup"><span data-stu-id="7cb40-135">INPUTS</span></span>

### <span data-ttu-id="7cb40-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7cb40-136">System.String</span></span>
<span data-ttu-id="7cb40-137">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="7cb40-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7cb40-138">출력</span><span class="sxs-lookup"><span data-stu-id="7cb40-138">OUTPUTS</span></span>

### <span data-ttu-id="7cb40-139">Microsoft. \* PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7cb40-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="7cb40-140">상속자</span><span class="sxs-lookup"><span data-stu-id="7cb40-140">NOTES</span></span>

## <span data-ttu-id="7cb40-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cb40-141">RELATED LINKS</span></span>

[<span data-ttu-id="7cb40-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7cb40-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="7cb40-143">제거-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7cb40-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="7cb40-144">새로운 AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cb40-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7cb40-145">추가-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cb40-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7cb40-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cb40-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7cb40-147">새로운 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7cb40-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7cb40-148">추가-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7cb40-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7cb40-149">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7cb40-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
