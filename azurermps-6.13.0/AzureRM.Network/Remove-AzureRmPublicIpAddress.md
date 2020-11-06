---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 6d294bd4b6f016ed1731a71528b39adc3bbe8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535751"
---
# <span data-ttu-id="1fe56-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1fe56-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="1fe56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fe56-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe56-103">공용 IP 주소를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fe56-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1fe56-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe56-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1fe56-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe56-106">**AzureRmPublicIpAddress** Cmdlet은 AZURE 공용 IP 주소를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="1fe56-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1fe56-107">EXAMPLES</span></span>

### <span data-ttu-id="1fe56-108">1: 공용 IP 주소 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="1fe56-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="1fe56-109">이 명령은 리소스 그룹 $rgName에서 $publicIpName 이라는 공용 IP 주소 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="1fe56-110">변수</span><span class="sxs-lookup"><span data-stu-id="1fe56-110">PARAMETERS</span></span>

### <span data-ttu-id="1fe56-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fe56-111">-AsJob</span></span>
<span data-ttu-id="1fe56-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1fe56-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fe56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe56-113">-DefaultProfile</span></span>
<span data-ttu-id="1fe56-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fe56-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1fe56-115">-Force</span></span>
<span data-ttu-id="1fe56-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1fe56-117">-이름</span><span class="sxs-lookup"><span data-stu-id="1fe56-117">-Name</span></span>
<span data-ttu-id="1fe56-118">이 cmdlet이 제거 하는 공용 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1fe56-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fe56-119">-PassThru</span></span>
<span data-ttu-id="1fe56-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1fe56-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1fe56-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe56-122">-ResourceGroupName</span></span>
<span data-ttu-id="1fe56-123">이 cmdlet이 제거할 공용 IP 주소를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1fe56-124">-확인</span><span class="sxs-lookup"><span data-stu-id="1fe56-124">-Confirm</span></span>
<span data-ttu-id="1fe56-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fe56-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe56-126">-WhatIf</span></span>
<span data-ttu-id="1fe56-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe56-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fe56-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe56-129">CommonParameters</span></span>
<span data-ttu-id="1fe56-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fe56-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe56-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe56-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe56-132">입력</span><span class="sxs-lookup"><span data-stu-id="1fe56-132">INPUTS</span></span>

### <span data-ttu-id="1fe56-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1fe56-133">System.String</span></span>

## <span data-ttu-id="1fe56-134">출력</span><span class="sxs-lookup"><span data-stu-id="1fe56-134">OUTPUTS</span></span>

### <span data-ttu-id="1fe56-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1fe56-135">System.Boolean</span></span>

## <span data-ttu-id="1fe56-136">상속자</span><span class="sxs-lookup"><span data-stu-id="1fe56-136">NOTES</span></span>

## <span data-ttu-id="1fe56-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fe56-137">RELATED LINKS</span></span>

[<span data-ttu-id="1fe56-138">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1fe56-138">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="1fe56-139">새로운 AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1fe56-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="1fe56-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1fe56-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


