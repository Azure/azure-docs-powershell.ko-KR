---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 0a7dc826aae7efebfc3d24bdeba02c75d0bf5a03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044524"
---
# <span data-ttu-id="c96c5-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="c96c5-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="c96c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c96c5-102">SYNOPSIS</span></span>
<span data-ttu-id="c96c5-103">미디어 서비스와 연결 된 REST 끝점에 액세스 하는 데 사용 되는 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="c96c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c96c5-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c96c5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c96c5-105">DESCRIPTION</span></span>
<span data-ttu-id="c96c5-106">**AzMediaServiceKey** cmdlet은 미디어 서비스와 연결 된 REST (Representational State Transfer) 끝점에 액세스 하는 데 사용 되는 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="c96c5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c96c5-107">EXAMPLES</span></span>

### <span data-ttu-id="c96c5-108">예제 1: 미디어 서비스에 액세스 하는 데 사용 되는 기본 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="c96c5-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="c96c5-109">이 명령은 ResourceGroup004 이라는 리소스 그룹에 속하는 MediaService001 이라는 미디어 서비스에 대 한 기본 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="c96c5-110">예제 2: 미디어 서비스에 액세스 하는 데 사용 되는 보조 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="c96c5-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="c96c5-111">이 명령은 Resourcegroup123 이라는 리소스 그룹에 속하는 MediaService002 이라는 미디어 서비스에 대 한 보조 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="c96c5-112">변수</span><span class="sxs-lookup"><span data-stu-id="c96c5-112">PARAMETERS</span></span>

### <span data-ttu-id="c96c5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c96c5-113">-AccountName</span></span>
<span data-ttu-id="c96c5-114">이 cmdlet이 다시 생성 하는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="c96c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c96c5-115">-DefaultProfile</span></span>
<span data-ttu-id="c96c5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c96c5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c96c5-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c96c5-117">-KeyType</span></span>
<span data-ttu-id="c96c5-118">미디어 서비스의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="c96c5-119">이 매개 변수에 허용 되는 값은 Primary 또는 Secondary입니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c96c5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c96c5-120">-ResourceGroupName</span></span>
<span data-ttu-id="c96c5-121">미디어 서비스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="c96c5-122">-확인</span><span class="sxs-lookup"><span data-stu-id="c96c5-122">-Confirm</span></span>
<span data-ttu-id="c96c5-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c96c5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c96c5-124">-WhatIf</span></span>
<span data-ttu-id="c96c5-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c96c5-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c96c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c96c5-127">CommonParameters</span></span>
<span data-ttu-id="c96c5-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c96c5-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c96c5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c96c5-130">입력</span><span class="sxs-lookup"><span data-stu-id="c96c5-130">INPUTS</span></span>

### <span data-ttu-id="c96c5-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c96c5-131">System.String</span></span>

## <span data-ttu-id="c96c5-132">출력</span><span class="sxs-lookup"><span data-stu-id="c96c5-132">OUTPUTS</span></span>

### <span data-ttu-id="c96c5-133">Microsoft. w i m.</span><span class="sxs-lookup"><span data-stu-id="c96c5-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="c96c5-134">상속자</span><span class="sxs-lookup"><span data-stu-id="c96c5-134">NOTES</span></span>

## <span data-ttu-id="c96c5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c96c5-135">RELATED LINKS</span></span>

[<span data-ttu-id="c96c5-136">Get-AzMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="c96c5-136">Get-AzMediaServiceKeys</span></span>](./Get-AzMediaServiceKeys.md)


