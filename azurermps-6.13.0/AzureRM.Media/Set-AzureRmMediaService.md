---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 3dfa3343edc82aaaf2c51a4e18ebc413ea3023c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530225"
---
# <span data-ttu-id="72cc5-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="72cc5-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="72cc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="72cc5-103">기존 미디어 서비스의 지정 된 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72cc5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72cc5-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72cc5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="72cc5-105">DESCRIPTION</span></span>
<span data-ttu-id="72cc5-106">**AzureRmMediaService** cmdlet은 기존 미디어 서비스의 지정 된 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="72cc5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="72cc5-107">EXAMPLES</span></span>

### <span data-ttu-id="72cc5-108">예제 1: 기존 미디어 서비스 수정</span><span class="sxs-lookup"><span data-stu-id="72cc5-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="72cc5-109">첫 번째 명령은 일련의 태그를 만들고이 태그를 $Tags 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="72cc5-110">이 두 번째 명령은 $Tags 변수에 저장 된 태그로 ResourceGroup123 이라는 리소스 그룹에 속하는 MediaService001 이라는 미디어 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="72cc5-111">이 명령은 $StorageAccounts 변수에 저장 된 저장소 구성 개체의 배열도 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="72cc5-112">변수</span><span class="sxs-lookup"><span data-stu-id="72cc5-112">PARAMETERS</span></span>

### <span data-ttu-id="72cc5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="72cc5-113">-AccountName</span></span>
<span data-ttu-id="72cc5-114">이 cmdlet이 수정 하는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="72cc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72cc5-115">-DefaultProfile</span></span>
<span data-ttu-id="72cc5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="72cc5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72cc5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72cc5-117">-ResourceGroupName</span></span>
<span data-ttu-id="72cc5-118">미디어 서비스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="72cc5-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="72cc5-119">-StorageAccounts</span></span>
<span data-ttu-id="72cc5-120">이 cmdlet이 미디어 서비스에 연결 하는 저장소 계정의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="72cc5-121">태그</span><span class="sxs-lookup"><span data-stu-id="72cc5-121">-Tag</span></span>
<span data-ttu-id="72cc5-122">미디어 계정과 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-122">The tags associated with the media account.</span></span>

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

### <span data-ttu-id="72cc5-123">-확인</span><span class="sxs-lookup"><span data-stu-id="72cc5-123">-Confirm</span></span>
<span data-ttu-id="72cc5-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72cc5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72cc5-125">-WhatIf</span></span>
<span data-ttu-id="72cc5-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72cc5-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72cc5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72cc5-128">CommonParameters</span></span>
<span data-ttu-id="72cc5-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72cc5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72cc5-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72cc5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72cc5-131">입력</span><span class="sxs-lookup"><span data-stu-id="72cc5-131">INPUTS</span></span>

### <span data-ttu-id="72cc5-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="72cc5-132">System.String</span></span>

### <span data-ttu-id="72cc5-133">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="72cc5-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="72cc5-134">Microsoft. Azure. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="72cc5-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="72cc5-135">출력</span><span class="sxs-lookup"><span data-stu-id="72cc5-135">OUTPUTS</span></span>

### <span data-ttu-id="72cc5-136">PSMediaService (\*).</span><span class="sxs-lookup"><span data-stu-id="72cc5-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="72cc5-137">상속자</span><span class="sxs-lookup"><span data-stu-id="72cc5-137">NOTES</span></span>

## <span data-ttu-id="72cc5-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72cc5-138">RELATED LINKS</span></span>

[<span data-ttu-id="72cc5-139">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="72cc5-139">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="72cc5-140">새로운 AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="72cc5-140">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="72cc5-141">제거-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="72cc5-141">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


