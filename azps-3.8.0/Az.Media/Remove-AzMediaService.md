---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044531"
---
# <span data-ttu-id="d5800-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d5800-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="d5800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5800-102">SYNOPSIS</span></span>
<span data-ttu-id="d5800-103">미디어 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5800-103">Removes a media service.</span></span>

## <span data-ttu-id="d5800-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5800-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5800-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d5800-105">DESCRIPTION</span></span>
<span data-ttu-id="d5800-106">**AzMediaService** cmdlet은 미디어 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5800-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="d5800-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d5800-107">EXAMPLES</span></span>

### <span data-ttu-id="d5800-108">예제 1: 미디어 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="d5800-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="d5800-109">이 명령은 ResourceGroup001 이라는 리소스 그룹에서 MediaService0011 이라는 미디어 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5800-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="d5800-110">변수</span><span class="sxs-lookup"><span data-stu-id="d5800-110">PARAMETERS</span></span>

### <span data-ttu-id="d5800-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d5800-111">-AccountName</span></span>
<span data-ttu-id="d5800-112">이 cmdlet이 제거 하는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5800-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5800-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5800-113">-DefaultProfile</span></span>
<span data-ttu-id="d5800-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d5800-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5800-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d5800-115">-Force</span></span>
<span data-ttu-id="d5800-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5800-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d5800-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5800-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5800-118">미디어 서비스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5800-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5800-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d5800-119">-Confirm</span></span>
<span data-ttu-id="d5800-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5800-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5800-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5800-121">-WhatIf</span></span>
<span data-ttu-id="d5800-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5800-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5800-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5800-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5800-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5800-124">CommonParameters</span></span>
<span data-ttu-id="d5800-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5800-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5800-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5800-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5800-127">입력</span><span class="sxs-lookup"><span data-stu-id="d5800-127">INPUTS</span></span>

### <span data-ttu-id="d5800-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d5800-128">System.String</span></span>

## <span data-ttu-id="d5800-129">출력</span><span class="sxs-lookup"><span data-stu-id="d5800-129">OUTPUTS</span></span>

### <span data-ttu-id="d5800-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d5800-130">System.Boolean</span></span>

## <span data-ttu-id="d5800-131">상속자</span><span class="sxs-lookup"><span data-stu-id="d5800-131">NOTES</span></span>

## <span data-ttu-id="d5800-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5800-132">RELATED LINKS</span></span>

[<span data-ttu-id="d5800-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d5800-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="d5800-134">새로운 AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d5800-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="d5800-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d5800-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


