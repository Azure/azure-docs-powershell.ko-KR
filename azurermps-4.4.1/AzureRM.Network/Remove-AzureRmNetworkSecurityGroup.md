---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: fd6d9a09bd2c4fa597d2c384d3ba8e730b3f1102
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702563"
---
# <span data-ttu-id="94ce6-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="94ce6-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="94ce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="94ce6-103">네트워크 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94ce6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94ce6-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94ce6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="94ce6-105">DESCRIPTION</span></span>
<span data-ttu-id="94ce6-106">**AzureRmNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="94ce6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="94ce6-107">EXAMPLES</span></span>

### <span data-ttu-id="94ce6-108">예제 1: 네트워크 보안 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="94ce6-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="94ce6-109">이 명령은 TestRG 이라는 리소스 그룹에 있는 NSG-FrontEnd 라는 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="94ce6-110">변수</span><span class="sxs-lookup"><span data-stu-id="94ce6-110">PARAMETERS</span></span>

### <span data-ttu-id="94ce6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="94ce6-111">-Force</span></span>
<span data-ttu-id="94ce6-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94ce6-113">-이름</span><span class="sxs-lookup"><span data-stu-id="94ce6-113">-Name</span></span>
<span data-ttu-id="94ce6-114">이 cmdlet이 제거 하는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-114">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="94ce6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94ce6-115">-PassThru</span></span>
<span data-ttu-id="94ce6-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="94ce6-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="94ce6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ce6-118">-ResourceGroupName</span></span>
<span data-ttu-id="94ce6-119">이 cmdlet이 네트워크 보안 그룹을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-119">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="94ce6-120">-확인</span><span class="sxs-lookup"><span data-stu-id="94ce6-120">-Confirm</span></span>
<span data-ttu-id="94ce6-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94ce6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94ce6-122">-WhatIf</span></span>
<span data-ttu-id="94ce6-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94ce6-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94ce6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ce6-125">-DefaultProfile</span></span>
<span data-ttu-id="94ce6-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94ce6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ce6-127">CommonParameters</span></span>
<span data-ttu-id="94ce6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94ce6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ce6-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94ce6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ce6-130">입력</span><span class="sxs-lookup"><span data-stu-id="94ce6-130">INPUTS</span></span>

## <span data-ttu-id="94ce6-131">출력</span><span class="sxs-lookup"><span data-stu-id="94ce6-131">OUTPUTS</span></span>

## <span data-ttu-id="94ce6-132">상속자</span><span class="sxs-lookup"><span data-stu-id="94ce6-132">NOTES</span></span>

## <span data-ttu-id="94ce6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94ce6-133">RELATED LINKS</span></span>

[<span data-ttu-id="94ce6-134">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="94ce6-134">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="94ce6-135">새로운 AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="94ce6-135">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="94ce6-136">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="94ce6-136">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


