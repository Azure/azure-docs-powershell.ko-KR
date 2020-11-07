---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: ba7bda62d0d001f11ff729ca0ecce6327b659855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869794"
---
# <span data-ttu-id="dcd88-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dcd88-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="dcd88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcd88-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd88-103">응용 프로그램 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-103">Removes an application gateway.</span></span>

## <span data-ttu-id="dcd88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dcd88-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd88-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dcd88-105">DESCRIPTION</span></span>
<span data-ttu-id="dcd88-106">**Remove-AzApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="dcd88-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dcd88-107">EXAMPLES</span></span>

### <span data-ttu-id="dcd88-108">예제 1: 지정 된 응용 프로그램 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="dcd88-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dcd88-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="dcd88-110">변수</span><span class="sxs-lookup"><span data-stu-id="dcd88-110">PARAMETERS</span></span>

### <span data-ttu-id="dcd88-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd88-111">-DefaultProfile</span></span>
<span data-ttu-id="dcd88-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcd88-113">-Force</span><span class="sxs-lookup"><span data-stu-id="dcd88-113">-Force</span></span>
<span data-ttu-id="dcd88-114">리소스가 할당 되었는지 여부에 관계 없이 cmdlet이 응용 프로그램 게이트웨이를 삭제 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd88-115">-이름</span><span class="sxs-lookup"><span data-stu-id="dcd88-115">-Name</span></span>
<span data-ttu-id="dcd88-116">제거할 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="dcd88-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcd88-117">-PassThru</span></span>
<span data-ttu-id="dcd88-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dcd88-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dcd88-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd88-120">-ResourceGroupName</span></span>
<span data-ttu-id="dcd88-121">응용 프로그램 게이트웨이가 속한 리소스 그룹 이름의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="dcd88-122">-확인</span><span class="sxs-lookup"><span data-stu-id="dcd88-122">-Confirm</span></span>
<span data-ttu-id="dcd88-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcd88-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd88-124">-WhatIf</span></span>
<span data-ttu-id="dcd88-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcd88-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcd88-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd88-127">CommonParameters</span></span>
<span data-ttu-id="dcd88-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd88-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd88-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcd88-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd88-130">입력</span><span class="sxs-lookup"><span data-stu-id="dcd88-130">INPUTS</span></span>

### <span data-ttu-id="dcd88-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dcd88-131">System.String</span></span>

### <span data-ttu-id="dcd88-132">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dcd88-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dcd88-133">출력</span><span class="sxs-lookup"><span data-stu-id="dcd88-133">OUTPUTS</span></span>

### <span data-ttu-id="dcd88-134">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="dcd88-134">System.Boolean</span></span>

## <span data-ttu-id="dcd88-135">상속자</span><span class="sxs-lookup"><span data-stu-id="dcd88-135">NOTES</span></span>

## <span data-ttu-id="dcd88-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dcd88-136">RELATED LINKS</span></span>

[<span data-ttu-id="dcd88-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dcd88-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


