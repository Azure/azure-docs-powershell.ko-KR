---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
ms.openlocfilehash: 8c2f6a45bb483109b61be47de3013f3ccb4d5c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533303"
---
# <span data-ttu-id="3d19f-101">Remove-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="3d19f-101">Remove-AzureRmSecurityContact</span></span>

## <span data-ttu-id="3d19f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d19f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d19f-103">보안 연락처를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d19f-103">Deletes a security contact.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d19f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d19f-104">SYNTAX</span></span>

### <span data-ttu-id="3d19f-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="3d19f-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d19f-106">리소스</span><span class="sxs-lookup"><span data-stu-id="3d19f-106">ResourceId</span></span>
```
Remove-AzureRmSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d19f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3d19f-107">InputObject</span></span>
```
Remove-AzureRmSecurityContact -InputObject <PSRemoveSecurityContactInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d19f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3d19f-108">DESCRIPTION</span></span>
<span data-ttu-id="3d19f-109">보안 연락처를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d19f-109">Deletes a security contact.</span></span>

## <span data-ttu-id="3d19f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3d19f-110">EXAMPLES</span></span>

### <span data-ttu-id="3d19f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3d19f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityContact -Name "default1"
```

<span data-ttu-id="3d19f-112">"Default1" 보안 연락처를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d19f-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="3d19f-113">변수</span><span class="sxs-lookup"><span data-stu-id="3d19f-113">PARAMETERS</span></span>

### <span data-ttu-id="3d19f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d19f-114">-DefaultProfile</span></span>
<span data-ttu-id="3d19f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d19f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d19f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d19f-116">-InputObject</span></span>
<span data-ttu-id="3d19f-117">입력 개체</span><span class="sxs-lookup"><span data-stu-id="3d19f-117">Input Object.</span></span>

```yaml
Type: PSRemoveSecurityContactInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d19f-118">-이름</span><span class="sxs-lookup"><span data-stu-id="3d19f-118">-Name</span></span>
<span data-ttu-id="3d19f-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d19f-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d19f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d19f-120">-PassThru</span></span>
<span data-ttu-id="3d19f-121">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d19f-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="3d19f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d19f-122">-ResourceId</span></span>
<span data-ttu-id="3d19f-123">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3d19f-123">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d19f-124">-확인</span><span class="sxs-lookup"><span data-stu-id="3d19f-124">-Confirm</span></span>
<span data-ttu-id="3d19f-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d19f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d19f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d19f-126">-WhatIf</span></span>
<span data-ttu-id="3d19f-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d19f-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d19f-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d19f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d19f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d19f-129">CommonParameters</span></span>
<span data-ttu-id="3d19f-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d19f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d19f-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d19f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d19f-132">입력</span><span class="sxs-lookup"><span data-stu-id="3d19f-132">INPUTS</span></span>

### <span data-ttu-id="3d19f-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d19f-133">System.String</span></span>
<span data-ttu-id="3d19f-134">PSRemoveSecurityContactInputObject의 보안. i a.</span><span class="sxs-lookup"><span data-stu-id="3d19f-134">Microsoft.Azure.Commands.Security.Cmdlets.SecurityContacts.PSRemoveSecurityContactInputObject</span></span>

## <span data-ttu-id="3d19f-135">출력</span><span class="sxs-lookup"><span data-stu-id="3d19f-135">OUTPUTS</span></span>

### <span data-ttu-id="3d19f-136">Microsoft. Azure. m a m a 연락처. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="3d19f-136">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="3d19f-137">상속자</span><span class="sxs-lookup"><span data-stu-id="3d19f-137">NOTES</span></span>

## <span data-ttu-id="3d19f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d19f-138">RELATED LINKS</span></span>
