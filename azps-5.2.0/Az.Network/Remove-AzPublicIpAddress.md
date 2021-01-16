---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352370"
---
# <span data-ttu-id="31818-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="31818-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="31818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31818-102">SYNOPSIS</span></span>
<span data-ttu-id="31818-103">공용 IP 주소를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="31818-103">Removes a public IP address.</span></span>

## <span data-ttu-id="31818-104">구문</span><span class="sxs-lookup"><span data-stu-id="31818-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31818-105">설명</span><span class="sxs-lookup"><span data-stu-id="31818-105">DESCRIPTION</span></span>
<span data-ttu-id="31818-106">**Remove-AzPublicIpAddress** cmdlet은 Azure 공용 IP 주소를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="31818-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="31818-107">예제</span><span class="sxs-lookup"><span data-stu-id="31818-107">EXAMPLES</span></span>

### <span data-ttu-id="31818-108">1: 공용 IP 주소 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="31818-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="31818-109">이 명령은 리소스 그룹 $publicIpName 이름의 공용 IP 주소 리소스를 $rgName.</span><span class="sxs-lookup"><span data-stu-id="31818-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="31818-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31818-110">PARAMETERS</span></span>

### <span data-ttu-id="31818-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31818-111">-AsJob</span></span>
<span data-ttu-id="31818-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="31818-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31818-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31818-113">-DefaultProfile</span></span>
<span data-ttu-id="31818-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31818-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31818-115">-Force</span><span class="sxs-lookup"><span data-stu-id="31818-115">-Force</span></span>
<span data-ttu-id="31818-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="31818-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="31818-117">-Name</span><span class="sxs-lookup"><span data-stu-id="31818-117">-Name</span></span>
<span data-ttu-id="31818-118">이 cmdlet에서 제거하는 공용 IP 주소의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="31818-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="31818-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31818-119">-PassThru</span></span>
<span data-ttu-id="31818-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="31818-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="31818-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31818-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="31818-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31818-122">-ResourceGroupName</span></span>
<span data-ttu-id="31818-123">이 cmdlet에서 제거하는 공용 IP 주소를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="31818-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="31818-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31818-124">-Confirm</span></span>
<span data-ttu-id="31818-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="31818-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31818-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31818-126">-WhatIf</span></span>
<span data-ttu-id="31818-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="31818-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31818-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31818-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31818-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31818-129">CommonParameters</span></span>
<span data-ttu-id="31818-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31818-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31818-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="31818-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31818-132">입력</span><span class="sxs-lookup"><span data-stu-id="31818-132">INPUTS</span></span>

### <span data-ttu-id="31818-133">System.String</span><span class="sxs-lookup"><span data-stu-id="31818-133">System.String</span></span>

## <span data-ttu-id="31818-134">출력</span><span class="sxs-lookup"><span data-stu-id="31818-134">OUTPUTS</span></span>

### <span data-ttu-id="31818-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31818-135">System.Boolean</span></span>

## <span data-ttu-id="31818-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31818-136">NOTES</span></span>

## <span data-ttu-id="31818-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31818-137">RELATED LINKS</span></span>

[<span data-ttu-id="31818-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="31818-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="31818-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="31818-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="31818-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="31818-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


