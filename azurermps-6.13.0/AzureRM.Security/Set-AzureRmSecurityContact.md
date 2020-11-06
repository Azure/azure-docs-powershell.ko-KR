---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
ms.openlocfilehash: 30586dcbbc08c31bf9b9fe65886fd2f487398618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530069"
---
# <span data-ttu-id="0942a-101">Set-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="0942a-101">Set-AzureRmSecurityContact</span></span>

## <span data-ttu-id="0942a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0942a-102">SYNOPSIS</span></span>
<span data-ttu-id="0942a-103">구독에 대 한 보안 연락처를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0942a-103">Updates a security contact for a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0942a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0942a-104">SYNTAX</span></span>

```
Set-AzureRmSecurityContact -Name <String> -Email <String> -Phone <String> [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0942a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0942a-105">DESCRIPTION</span></span>
<span data-ttu-id="0942a-106">구독에 대 한 보안 연락처를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0942a-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="0942a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0942a-107">EXAMPLES</span></span>

### <span data-ttu-id="0942a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0942a-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="0942a-109">구독에 대 한 보안 연락처를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0942a-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="0942a-110">변수</span><span class="sxs-lookup"><span data-stu-id="0942a-110">PARAMETERS</span></span>

### <span data-ttu-id="0942a-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="0942a-111">-AlertAdmin</span></span>
<span data-ttu-id="0942a-112">관리자에 게 알림이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0942a-112">Alerts To Administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0942a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0942a-113">-DefaultProfile</span></span>
<span data-ttu-id="0942a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0942a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0942a-115">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="0942a-115">-Email</span></span>
<span data-ttu-id="0942a-116">이메일.</span><span class="sxs-lookup"><span data-stu-id="0942a-116">E-Mail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0942a-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0942a-117">-Name</span></span>
<span data-ttu-id="0942a-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0942a-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0942a-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="0942a-119">-NotifyOnAlert</span></span>
<span data-ttu-id="0942a-120">알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="0942a-120">Alert Notifications.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0942a-121">-전화</span><span class="sxs-lookup"><span data-stu-id="0942a-121">-Phone</span></span>
<span data-ttu-id="0942a-122">전화.</span><span class="sxs-lookup"><span data-stu-id="0942a-122">Phone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0942a-123">-확인</span><span class="sxs-lookup"><span data-stu-id="0942a-123">-Confirm</span></span>
<span data-ttu-id="0942a-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0942a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0942a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0942a-125">-WhatIf</span></span>
<span data-ttu-id="0942a-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0942a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0942a-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0942a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0942a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0942a-128">CommonParameters</span></span>
<span data-ttu-id="0942a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0942a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0942a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0942a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0942a-131">입력</span><span class="sxs-lookup"><span data-stu-id="0942a-131">INPUTS</span></span>

### <span data-ttu-id="0942a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0942a-132">System.String</span></span>

## <span data-ttu-id="0942a-133">출력</span><span class="sxs-lookup"><span data-stu-id="0942a-133">OUTPUTS</span></span>

### <span data-ttu-id="0942a-134">Microsoft. Azure. m a m a 연락처. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="0942a-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="0942a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="0942a-135">NOTES</span></span>

## <span data-ttu-id="0942a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0942a-136">RELATED LINKS</span></span>
