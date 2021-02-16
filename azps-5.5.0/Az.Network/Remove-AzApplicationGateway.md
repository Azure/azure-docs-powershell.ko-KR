---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191801"
---
# <span data-ttu-id="fa2be-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fa2be-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="fa2be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa2be-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2be-103">애플리케이션 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-103">Removes an application gateway.</span></span>

## <span data-ttu-id="fa2be-104">구문</span><span class="sxs-lookup"><span data-stu-id="fa2be-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa2be-105">설명</span><span class="sxs-lookup"><span data-stu-id="fa2be-105">DESCRIPTION</span></span>
<span data-ttu-id="fa2be-106">**Remove-AzApplicationGateway** cmdlet은 애플리케이션 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="fa2be-107">예제</span><span class="sxs-lookup"><span data-stu-id="fa2be-107">EXAMPLES</span></span>

### <span data-ttu-id="fa2be-108">예제 1: 지정된 애플리케이션 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="fa2be-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fa2be-109">이 명령은 ResourceGroup01이라는 리소스 그룹에서 ApplicationGateway01이라는 애플리케이션 게이트웨이를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="fa2be-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa2be-110">PARAMETERS</span></span>

### <span data-ttu-id="fa2be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2be-111">-DefaultProfile</span></span>
<span data-ttu-id="fa2be-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa2be-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fa2be-113">-Force</span></span>
<span data-ttu-id="fa2be-114">cmdlet이 리소스가 할당되어 있는지 여부에 관계없이 애플리케이션 게이트웨이를 강제로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="fa2be-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fa2be-115">-Name</span></span>
<span data-ttu-id="fa2be-116">제거할 애플리케이션 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="fa2be-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa2be-117">-PassThru</span></span>
<span data-ttu-id="fa2be-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa2be-119">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa2be-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa2be-120">-ResourceGroupName</span></span>
<span data-ttu-id="fa2be-121">애플리케이션 게이트웨이가 속한 리소스 그룹 이름의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="fa2be-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa2be-122">-Confirm</span></span>
<span data-ttu-id="fa2be-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa2be-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa2be-124">-WhatIf</span></span>
<span data-ttu-id="fa2be-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fa2be-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa2be-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa2be-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2be-127">CommonParameters</span></span>
<span data-ttu-id="fa2be-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2be-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2be-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fa2be-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2be-130">입력</span><span class="sxs-lookup"><span data-stu-id="fa2be-130">INPUTS</span></span>

### <span data-ttu-id="fa2be-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fa2be-131">System.String</span></span>

### <span data-ttu-id="fa2be-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa2be-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fa2be-133">출력</span><span class="sxs-lookup"><span data-stu-id="fa2be-133">OUTPUTS</span></span>

### <span data-ttu-id="fa2be-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa2be-134">System.Boolean</span></span>

## <span data-ttu-id="fa2be-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fa2be-135">NOTES</span></span>

## <span data-ttu-id="fa2be-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa2be-136">RELATED LINKS</span></span>

[<span data-ttu-id="fa2be-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fa2be-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


