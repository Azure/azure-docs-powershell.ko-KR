---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: f8a509fc73387361de5bd191ee9eefc61c33a5f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996128"
---
# <span data-ttu-id="cbc52-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cbc52-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="cbc52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbc52-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc52-103">공용 IP 주소를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-103">Removes a public IP address.</span></span>

## <span data-ttu-id="cbc52-104">구문</span><span class="sxs-lookup"><span data-stu-id="cbc52-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbc52-105">설명</span><span class="sxs-lookup"><span data-stu-id="cbc52-105">DESCRIPTION</span></span>
<span data-ttu-id="cbc52-106">**Remove-AzPublicIpAddress** cmdlet은 Azure 공용 IP 주소를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="cbc52-107">예제</span><span class="sxs-lookup"><span data-stu-id="cbc52-107">EXAMPLES</span></span>

### <span data-ttu-id="cbc52-108">1: 공용 IP 주소 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="cbc52-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="cbc52-109">이 명령은 리소스 그룹에서 $publicIpName라는 공용 IP 주소 리소스를 $rgName.</span><span class="sxs-lookup"><span data-stu-id="cbc52-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="cbc52-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cbc52-110">PARAMETERS</span></span>

### <span data-ttu-id="cbc52-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbc52-111">-AsJob</span></span>
<span data-ttu-id="cbc52-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cbc52-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbc52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc52-113">-DefaultProfile</span></span>
<span data-ttu-id="cbc52-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbc52-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cbc52-115">-Force</span></span>
<span data-ttu-id="cbc52-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cbc52-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cbc52-117">-Name</span></span>
<span data-ttu-id="cbc52-118">이 cmdlet이 제거한 공용 IP 주소의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cbc52-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbc52-119">-PassThru</span></span>
<span data-ttu-id="cbc52-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cbc52-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cbc52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbc52-122">-ResourceGroupName</span></span>
<span data-ttu-id="cbc52-123">이 cmdlet이 제거한 공용 IP 주소를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cbc52-124">-확인</span><span class="sxs-lookup"><span data-stu-id="cbc52-124">-Confirm</span></span>
<span data-ttu-id="cbc52-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbc52-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbc52-126">-WhatIf</span></span>
<span data-ttu-id="cbc52-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbc52-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbc52-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc52-129">CommonParameters</span></span>
<span data-ttu-id="cbc52-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc52-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc52-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cbc52-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc52-132">입력</span><span class="sxs-lookup"><span data-stu-id="cbc52-132">INPUTS</span></span>

### <span data-ttu-id="cbc52-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cbc52-133">System.String</span></span>

## <span data-ttu-id="cbc52-134">출력</span><span class="sxs-lookup"><span data-stu-id="cbc52-134">OUTPUTS</span></span>

### <span data-ttu-id="cbc52-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbc52-135">System.Boolean</span></span>

## <span data-ttu-id="cbc52-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cbc52-136">NOTES</span></span>

## <span data-ttu-id="cbc52-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbc52-137">RELATED LINKS</span></span>

[<span data-ttu-id="cbc52-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cbc52-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="cbc52-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cbc52-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="cbc52-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cbc52-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


