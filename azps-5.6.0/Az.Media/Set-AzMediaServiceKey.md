---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 43e98ae0c6aa05123a291704baeb5855e8e3b1af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982987"
---
# <span data-ttu-id="8cbd8-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="8cbd8-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="8cbd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cbd8-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbd8-103">미디어 서비스와 연결된 REST 엔드포인트에 액세스하는 데 사용되는 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="8cbd8-104">구문</span><span class="sxs-lookup"><span data-stu-id="8cbd8-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cbd8-105">설명</span><span class="sxs-lookup"><span data-stu-id="8cbd8-105">DESCRIPTION</span></span>
<span data-ttu-id="8cbd8-106">**Set-AzMediaServiceKey** cmdlet은 미디어 서비스에 연결된 REST(표현 상태 전송) 엔드포인트에 액세스하는 데 사용되는 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="8cbd8-107">예제</span><span class="sxs-lookup"><span data-stu-id="8cbd8-107">EXAMPLES</span></span>

### <span data-ttu-id="8cbd8-108">예제 1: Media Service에 액세스하는 데 사용되는 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="8cbd8-109">이 명령은 ResourceGroup004라는 리소스 그룹에 속하는 MediaService001이라는 미디어 서비스의 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="8cbd8-110">예제 2: Media Service에 액세스하는 데 사용되는 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="8cbd8-111">이 명령은 Resourcegroup123이라는 리소스 그룹에 속하는 MediaService002라는 미디어 서비스의 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="8cbd8-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8cbd8-112">PARAMETERS</span></span>

### <span data-ttu-id="8cbd8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8cbd8-113">-AccountName</span></span>
<span data-ttu-id="8cbd8-114">이 cmdlet이 다시 생성하는 미디어 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="8cbd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbd8-115">-DefaultProfile</span></span>
<span data-ttu-id="8cbd8-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8cbd8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cbd8-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="8cbd8-117">-KeyType</span></span>
<span data-ttu-id="8cbd8-118">미디어 서비스의 키 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="8cbd8-119">이 매개 변수에 대해 허용되는 값은 기본 또는 보조 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="8cbd8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cbd8-120">-ResourceGroupName</span></span>
<span data-ttu-id="8cbd8-121">미디어 서비스를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="8cbd8-122">-확인</span><span class="sxs-lookup"><span data-stu-id="8cbd8-122">-Confirm</span></span>
<span data-ttu-id="8cbd8-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cbd8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cbd8-124">-WhatIf</span></span>
<span data-ttu-id="8cbd8-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cbd8-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cbd8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbd8-127">CommonParameters</span></span>
<span data-ttu-id="8cbd8-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbd8-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbd8-130">입력</span><span class="sxs-lookup"><span data-stu-id="8cbd8-130">INPUTS</span></span>

### <span data-ttu-id="8cbd8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8cbd8-131">System.String</span></span>

## <span data-ttu-id="8cbd8-132">출력</span><span class="sxs-lookup"><span data-stu-id="8cbd8-132">OUTPUTS</span></span>

### <span data-ttu-id="8cbd8-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="8cbd8-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="8cbd8-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8cbd8-134">NOTES</span></span>

## <span data-ttu-id="8cbd8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cbd8-135">RELATED LINKS</span></span>

[<span data-ttu-id="8cbd8-136">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="8cbd8-136">Get-AzMediaServiceKey</span></span>](./Get-AzMediaServiceKey.md)


