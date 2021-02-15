---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203626"
---
# <span data-ttu-id="2e130-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2e130-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="2e130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e130-102">SYNOPSIS</span></span>
<span data-ttu-id="2e130-103">미디어 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2e130-103">Removes a media service.</span></span>

## <span data-ttu-id="2e130-104">구문</span><span class="sxs-lookup"><span data-stu-id="2e130-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e130-105">설명</span><span class="sxs-lookup"><span data-stu-id="2e130-105">DESCRIPTION</span></span>
<span data-ttu-id="2e130-106">**Remove-AzMediaService** cmdlet은 미디어 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2e130-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="2e130-107">예제</span><span class="sxs-lookup"><span data-stu-id="2e130-107">EXAMPLES</span></span>

### <span data-ttu-id="2e130-108">예제 1: 미디어 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="2e130-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="2e130-109">이 명령은 ResourceGroup001이라는 리소스 그룹에서 MediaService0011이라는 미디어 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2e130-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="2e130-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e130-110">PARAMETERS</span></span>

### <span data-ttu-id="2e130-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2e130-111">-AccountName</span></span>
<span data-ttu-id="2e130-112">이 cmdlet이 제거하는 미디어 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e130-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2e130-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e130-113">-DefaultProfile</span></span>
<span data-ttu-id="2e130-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2e130-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e130-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2e130-115">-Force</span></span>
<span data-ttu-id="2e130-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2e130-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2e130-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e130-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e130-118">미디어 서비스를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e130-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="2e130-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e130-119">-Confirm</span></span>
<span data-ttu-id="2e130-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e130-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e130-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e130-121">-WhatIf</span></span>
<span data-ttu-id="2e130-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2e130-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e130-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e130-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e130-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e130-124">CommonParameters</span></span>
<span data-ttu-id="2e130-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2e130-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e130-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2e130-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e130-127">입력</span><span class="sxs-lookup"><span data-stu-id="2e130-127">INPUTS</span></span>

### <span data-ttu-id="2e130-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2e130-128">System.String</span></span>

## <span data-ttu-id="2e130-129">출력</span><span class="sxs-lookup"><span data-stu-id="2e130-129">OUTPUTS</span></span>

### <span data-ttu-id="2e130-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e130-130">System.Boolean</span></span>

## <span data-ttu-id="2e130-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2e130-131">NOTES</span></span>

## <span data-ttu-id="2e130-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e130-132">RELATED LINKS</span></span>

[<span data-ttu-id="2e130-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2e130-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="2e130-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2e130-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="2e130-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2e130-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


