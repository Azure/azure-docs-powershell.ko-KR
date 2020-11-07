---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 9507cc178613a80ff0d49ed62e7e43698f5f1d7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703699"
---
# <span data-ttu-id="efcce-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="efcce-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="efcce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efcce-102">SYNOPSIS</span></span>
<span data-ttu-id="efcce-103">미디어 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efcce-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efcce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efcce-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efcce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="efcce-105">DESCRIPTION</span></span>
<span data-ttu-id="efcce-106">**AzureRmMediaService** cmdlet은 미디어 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efcce-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="efcce-107">예제의</span><span class="sxs-lookup"><span data-stu-id="efcce-107">EXAMPLES</span></span>

### <span data-ttu-id="efcce-108">예제 1: 미디어 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="efcce-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="efcce-109">이 명령은 ResourceGroup001 이라는 리소스 그룹에서 MediaService0011 이라는 미디어 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efcce-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="efcce-110">변수</span><span class="sxs-lookup"><span data-stu-id="efcce-110">PARAMETERS</span></span>

### <span data-ttu-id="efcce-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="efcce-111">-AccountName</span></span>
<span data-ttu-id="efcce-112">이 cmdlet이 제거 하는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efcce-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="efcce-113">-Force</span><span class="sxs-lookup"><span data-stu-id="efcce-113">-Force</span></span>
<span data-ttu-id="efcce-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="efcce-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="efcce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efcce-115">-ResourceGroupName</span></span>
<span data-ttu-id="efcce-116">미디어 서비스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efcce-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="efcce-117">-확인</span><span class="sxs-lookup"><span data-stu-id="efcce-117">-Confirm</span></span>
<span data-ttu-id="efcce-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="efcce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efcce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efcce-119">-WhatIf</span></span>
<span data-ttu-id="efcce-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="efcce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efcce-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efcce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efcce-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efcce-122">-DefaultProfile</span></span>
<span data-ttu-id="efcce-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efcce-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efcce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efcce-124">CommonParameters</span></span>
<span data-ttu-id="efcce-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efcce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efcce-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efcce-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efcce-127">입력</span><span class="sxs-lookup"><span data-stu-id="efcce-127">INPUTS</span></span>

## <span data-ttu-id="efcce-128">출력</span><span class="sxs-lookup"><span data-stu-id="efcce-128">OUTPUTS</span></span>

### <span data-ttu-id="efcce-129">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="efcce-129">System.Boolean</span></span>

## <span data-ttu-id="efcce-130">상속자</span><span class="sxs-lookup"><span data-stu-id="efcce-130">NOTES</span></span>

## <span data-ttu-id="efcce-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efcce-131">RELATED LINKS</span></span>

[<span data-ttu-id="efcce-132">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="efcce-132">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="efcce-133">새로운 AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="efcce-133">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="efcce-134">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="efcce-134">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


