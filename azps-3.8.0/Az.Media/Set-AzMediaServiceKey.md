---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 85f8b91fd99da5d5b014d74ff8fadd225ab0c2c7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409276"
---
# <span data-ttu-id="d8a17-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="d8a17-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="d8a17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8a17-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a17-103">미디어 서비스에 연결된 REST 엔드포인트에 액세스하는 데 사용되는 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="d8a17-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8a17-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8a17-105">설명</span><span class="sxs-lookup"><span data-stu-id="d8a17-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a17-106">**Set-AzMediaServiceKey** cmdlet은 미디어 서비스에 연결된 REST(Representational State Transfer) 엔드포인트에 액세스하는 데 사용되는 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="d8a17-107">예제</span><span class="sxs-lookup"><span data-stu-id="d8a17-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a17-108">예제 1: Media Service에 액세스하는 데 사용되는 기본 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="d8a17-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="d8a17-109">이 명령은 ResourceGroup004라는 리소스 그룹에 속하는 MediaService001이라는 미디어 서비스에 대한 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="d8a17-110">예제 2: Media Service에 액세스하는 데 사용되는 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="d8a17-111">이 명령은 Resourcegroup123이라는 리소스 그룹에 속하는 MediaService002라는 미디어 서비스에 대한 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="d8a17-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8a17-112">PARAMETERS</span></span>

### <span data-ttu-id="d8a17-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d8a17-113">-AccountName</span></span>
<span data-ttu-id="d8a17-114">이 cmdlet이 다시 생성하는 미디어 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="d8a17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a17-115">-DefaultProfile</span></span>
<span data-ttu-id="d8a17-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d8a17-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8a17-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d8a17-117">-KeyType</span></span>
<span data-ttu-id="d8a17-118">미디어 서비스의 키 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="d8a17-119">이 매개 변수에 허용되는 값은 기본 또는 보조입니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="d8a17-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8a17-120">-ResourceGroupName</span></span>
<span data-ttu-id="d8a17-121">미디어 서비스를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="d8a17-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8a17-122">-Confirm</span></span>
<span data-ttu-id="d8a17-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8a17-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8a17-124">-WhatIf</span></span>
<span data-ttu-id="d8a17-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d8a17-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8a17-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8a17-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a17-127">CommonParameters</span></span>
<span data-ttu-id="d8a17-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8a17-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a17-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d8a17-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a17-130">입력</span><span class="sxs-lookup"><span data-stu-id="d8a17-130">INPUTS</span></span>

### <span data-ttu-id="d8a17-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d8a17-131">System.String</span></span>

## <span data-ttu-id="d8a17-132">출력</span><span class="sxs-lookup"><span data-stu-id="d8a17-132">OUTPUTS</span></span>

### <span data-ttu-id="d8a17-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="d8a17-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="d8a17-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8a17-134">NOTES</span></span>

## <span data-ttu-id="d8a17-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8a17-135">RELATED LINKS</span></span>



