---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 1c6f6a38c1811bdda32b60d4af1707c78eb7afd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702581"
---
# <span data-ttu-id="1dc4c-101">Remove-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="1dc4c-101">Remove-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="1dc4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc4c-103">이 구독에 대 한 보안 작업 영역 설정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-103">Deletes the security workspace setting for this subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dc4c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1dc4c-104">SYNTAX</span></span>

### <span data-ttu-id="1dc4c-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="1dc4c-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc4c-106">리소스</span><span class="sxs-lookup"><span data-stu-id="1dc4c-106">ResourceId</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc4c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1dc4c-107">InputObject</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -InputObject <PSRemoveWorkspaceSettingInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc4c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1dc4c-108">DESCRIPTION</span></span>
<span data-ttu-id="1dc4c-109">이 구독에 대 한 보안 작업 영역 설정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="1dc4c-110">이 작업을 수행 하면 새로 설치 된 보안 에이전트가이 susbscription의 기본 작업 영역에 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-110">This action will make the newly installed security agents to report to the default workspace of this susbscription.</span></span>

## <span data-ttu-id="1dc4c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1dc4c-111">EXAMPLES</span></span>

### <span data-ttu-id="1dc4c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1dc4c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="1dc4c-113">이 구독에 대 한 보안 작업 영역 설정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="1dc4c-114">변수</span><span class="sxs-lookup"><span data-stu-id="1dc4c-114">PARAMETERS</span></span>

### <span data-ttu-id="1dc4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc4c-115">-DefaultProfile</span></span>
<span data-ttu-id="1dc4c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dc4c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dc4c-117">-InputObject</span></span>
<span data-ttu-id="1dc4c-118">입력 개체</span><span class="sxs-lookup"><span data-stu-id="1dc4c-118">Input Object.</span></span>

```yaml
Type: PSRemoveWorkspaceSettingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc4c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1dc4c-119">-Name</span></span>
<span data-ttu-id="1dc4c-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-120">Resource name.</span></span>

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

### <span data-ttu-id="1dc4c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dc4c-121">-PassThru</span></span>
<span data-ttu-id="1dc4c-122">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="1dc4c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dc4c-123">-ResourceId</span></span>
<span data-ttu-id="1dc4c-124">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-124">Resource ID.</span></span>

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

### <span data-ttu-id="1dc4c-125">-확인</span><span class="sxs-lookup"><span data-stu-id="1dc4c-125">-Confirm</span></span>
<span data-ttu-id="1dc4c-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc4c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc4c-127">-WhatIf</span></span>
<span data-ttu-id="1dc4c-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dc4c-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc4c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc4c-130">CommonParameters</span></span>
<span data-ttu-id="1dc4c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc4c-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc4c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc4c-133">입력</span><span class="sxs-lookup"><span data-stu-id="1dc4c-133">INPUTS</span></span>

### <span data-ttu-id="1dc4c-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1dc4c-134">System.String</span></span>
<span data-ttu-id="1dc4c-135">WorkspaceSettings. PSRemoveWorkspaceSettingInputObject에 대 한</span><span class="sxs-lookup"><span data-stu-id="1dc4c-135">Microsoft.Azure.Commands.Security.Cmdlets.WorkspaceSettings.PSRemoveWorkspaceSettingInputObject</span></span>

## <span data-ttu-id="1dc4c-136">출력</span><span class="sxs-lookup"><span data-stu-id="1dc4c-136">OUTPUTS</span></span>

### <span data-ttu-id="1dc4c-137">WorkspaceSettings. PSSecurityWorkspaceSetting에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="1dc4c-137">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="1dc4c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="1dc4c-138">NOTES</span></span>

## <span data-ttu-id="1dc4c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dc4c-139">RELATED LINKS</span></span>
