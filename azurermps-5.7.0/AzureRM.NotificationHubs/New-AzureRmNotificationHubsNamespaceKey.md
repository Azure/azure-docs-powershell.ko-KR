---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: 4756402ab46deb0260db19474a26e2c568055187
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535928"
---
# <span data-ttu-id="02c3c-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="02c3c-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="02c3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="02c3c-103">네임 스페이스에 대 한 권한 부여 규칙 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c3c-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02c3c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02c3c-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c3c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="02c3c-105">DESCRIPTION</span></span>
<span data-ttu-id="02c3c-106">New-AzureRmNotificationHubNamespaceKey cmdlet은 네임 스페이스 권한 부여 규칙에 대 한 기본 키/보조 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c3c-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="02c3c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="02c3c-107">EXAMPLES</span></span>

### <span data-ttu-id="02c3c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="02c3c-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="02c3c-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="02c3c-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="02c3c-110">변수</span><span class="sxs-lookup"><span data-stu-id="02c3c-110">PARAMETERS</span></span>

### <span data-ttu-id="02c3c-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="02c3c-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c3c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c3c-112">-DefaultProfile</span></span>
<span data-ttu-id="02c3c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="02c3c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c3c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="02c3c-114">-Force</span></span>
<span data-ttu-id="02c3c-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02c3c-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c3c-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="02c3c-116">-Namespace</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c3c-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="02c3c-117">-PolicyKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c3c-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="02c3c-118">-ResourceGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c3c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="02c3c-119">-Confirm</span></span>
<span data-ttu-id="02c3c-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c3c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c3c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c3c-121">-WhatIf</span></span>
<span data-ttu-id="02c3c-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02c3c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c3c-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02c3c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c3c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c3c-124">CommonParameters</span></span>
<span data-ttu-id="02c3c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c3c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c3c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c3c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c3c-127">입력</span><span class="sxs-lookup"><span data-stu-id="02c3c-127">INPUTS</span></span>

### <span data-ttu-id="02c3c-128">않아야</span><span class="sxs-lookup"><span data-stu-id="02c3c-128">None</span></span>
<span data-ttu-id="02c3c-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02c3c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02c3c-130">출력</span><span class="sxs-lookup"><span data-stu-id="02c3c-130">OUTPUTS</span></span>

### <span data-ttu-id="02c3c-131">Microsoft. 관리.. i g m. 목록 키</span><span class="sxs-lookup"><span data-stu-id="02c3c-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="02c3c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="02c3c-132">NOTES</span></span>

## <span data-ttu-id="02c3c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02c3c-133">RELATED LINKS</span></span>

