---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 396f603c4a4126b8d438f0048677da7a5dbd7492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530766"
---
# <span data-ttu-id="c4cf8-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4cf8-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="c4cf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="c4cf8-103">공용 IP 주소를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4cf8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4cf8-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4cf8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c4cf8-105">DESCRIPTION</span></span>
<span data-ttu-id="c4cf8-106">**AzureRmPublicIpAddress** Cmdlet은 AZURE 공용 IP 주소를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="c4cf8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c4cf8-107">EXAMPLES</span></span>

### <span data-ttu-id="c4cf8-108">1: 공용 IP 주소 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="c4cf8-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="c4cf8-109">이 명령은 리소스 그룹 $rgName에서 $publicIpName 이라는 공용 IP 주소 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="c4cf8-110">변수</span><span class="sxs-lookup"><span data-stu-id="c4cf8-110">PARAMETERS</span></span>

### <span data-ttu-id="c4cf8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c4cf8-111">-Force</span></span>
<span data-ttu-id="c4cf8-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4cf8-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c4cf8-113">-Name</span></span>
<span data-ttu-id="c4cf8-114">이 cmdlet이 제거 하는 공용 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-114">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c4cf8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4cf8-115">-PassThru</span></span>
<span data-ttu-id="c4cf8-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c4cf8-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c4cf8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4cf8-118">-ResourceGroupName</span></span>
<span data-ttu-id="c4cf8-119">이 cmdlet이 제거할 공용 IP 주소를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-119">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c4cf8-120">-확인</span><span class="sxs-lookup"><span data-stu-id="c4cf8-120">-Confirm</span></span>
<span data-ttu-id="c4cf8-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4cf8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4cf8-122">-WhatIf</span></span>
<span data-ttu-id="c4cf8-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4cf8-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4cf8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4cf8-125">-DefaultProfile</span></span>
<span data-ttu-id="c4cf8-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4cf8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4cf8-127">CommonParameters</span></span>
<span data-ttu-id="c4cf8-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4cf8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4cf8-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4cf8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4cf8-130">입력</span><span class="sxs-lookup"><span data-stu-id="c4cf8-130">INPUTS</span></span>

## <span data-ttu-id="c4cf8-131">출력</span><span class="sxs-lookup"><span data-stu-id="c4cf8-131">OUTPUTS</span></span>

## <span data-ttu-id="c4cf8-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c4cf8-132">NOTES</span></span>

## <span data-ttu-id="c4cf8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4cf8-133">RELATED LINKS</span></span>

[<span data-ttu-id="c4cf8-134">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4cf8-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c4cf8-135">새로운 AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4cf8-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c4cf8-136">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4cf8-136">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


