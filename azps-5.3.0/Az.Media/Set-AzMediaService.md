---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 5b85e3e64b4a79b33975d9b29d0498ac8ae0ce03
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496756"
---
# <span data-ttu-id="b7a17-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b7a17-101">Set-AzMediaService</span></span>

## <span data-ttu-id="b7a17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7a17-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a17-103">기존 미디어 서비스의 지정된 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a17-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="b7a17-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7a17-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7a17-105">설명</span><span class="sxs-lookup"><span data-stu-id="b7a17-105">DESCRIPTION</span></span>
<span data-ttu-id="b7a17-106">**Set-AzMediaService** cmdlet은 기존 미디어 서비스의 지정된 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a17-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="b7a17-107">예제</span><span class="sxs-lookup"><span data-stu-id="b7a17-107">EXAMPLES</span></span>

### <span data-ttu-id="b7a17-108">예제 1: 기존 미디어 서비스 수정</span><span class="sxs-lookup"><span data-stu-id="b7a17-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="b7a17-109">첫 번째 명령은 일련의 태그를 만들고 해당 태그를 $Tags.</span><span class="sxs-lookup"><span data-stu-id="b7a17-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="b7a17-110">이 두 번째 명령은 ResourceGroup123이라는 리소스 그룹에 속하는 MediaService001이라는 미디어 서비스를 변수에 저장된 태그로 $Tags 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a17-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="b7a17-111">또한 이 명령은 변수에 저장된 저장소 구성 개체의 배열을 $StorageAccounts 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a17-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="b7a17-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7a17-112">PARAMETERS</span></span>

### <span data-ttu-id="b7a17-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b7a17-113">-AccountName</span></span>
<span data-ttu-id="b7a17-114">이 cmdlet이 수정하는 미디어 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a17-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b7a17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a17-115">-DefaultProfile</span></span>
<span data-ttu-id="b7a17-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b7a17-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7a17-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a17-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7a17-118">미디어 서비스를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a17-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="b7a17-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="b7a17-119">-StorageAccounts</span></span>
<span data-ttu-id="b7a17-120">이 cmdlet이 미디어 서비스에 연결되는 저장소 계정의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a17-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a17-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7a17-121">-Tag</span></span>
<span data-ttu-id="b7a17-122">미디어 계정과 연결된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="b7a17-122">The tags associated with the media account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a17-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7a17-123">-Confirm</span></span>
<span data-ttu-id="b7a17-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7a17-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7a17-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7a17-125">-WhatIf</span></span>
<span data-ttu-id="b7a17-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b7a17-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7a17-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7a17-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7a17-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a17-128">CommonParameters</span></span>
<span data-ttu-id="b7a17-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a17-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a17-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b7a17-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a17-131">입력</span><span class="sxs-lookup"><span data-stu-id="b7a17-131">INPUTS</span></span>

### <span data-ttu-id="b7a17-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b7a17-132">System.String</span></span>

### <span data-ttu-id="b7a17-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7a17-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b7a17-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="b7a17-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="b7a17-135">출력</span><span class="sxs-lookup"><span data-stu-id="b7a17-135">OUTPUTS</span></span>

### <span data-ttu-id="b7a17-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="b7a17-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="b7a17-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7a17-137">NOTES</span></span>

## <span data-ttu-id="b7a17-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7a17-138">RELATED LINKS</span></span>

[<span data-ttu-id="b7a17-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b7a17-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="b7a17-140">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b7a17-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="b7a17-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b7a17-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


