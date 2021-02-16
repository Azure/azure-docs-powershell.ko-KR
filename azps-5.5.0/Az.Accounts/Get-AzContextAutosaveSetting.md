---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 193a1dab5bd08489740d0d95f65c6aad1ea85e43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199932"
---
# <span data-ttu-id="31536-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="31536-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="31536-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31536-102">SYNOPSIS</span></span>
<span data-ttu-id="31536-103">컨텍스트가 자동으로 저장되는지 여부 및 저장된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함하여 컨텍스트 자동 저장 기능에 대한 메타데이터를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="31536-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="31536-104">구문</span><span class="sxs-lookup"><span data-stu-id="31536-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31536-105">설명</span><span class="sxs-lookup"><span data-stu-id="31536-105">DESCRIPTION</span></span>
<span data-ttu-id="31536-106">컨텍스트가 자동으로 저장되는지 여부 및 저장된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함하여 컨텍스트 자동 저장 기능에 대한 메타데이터를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="31536-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="31536-107">예제</span><span class="sxs-lookup"><span data-stu-id="31536-107">EXAMPLES</span></span>

### <span data-ttu-id="31536-108">현재 세션에 대한 컨텍스트 저장 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31536-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="31536-109">컨텍스트가 저장되는 위치와 여부에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31536-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="31536-110">위의 예제에서는 자동 자동 조정 기능을 사용하지 않도록 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="31536-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="31536-111">현재 사용자에 대한 컨텍스트 저장 메타데이터를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31536-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="31536-112">기본적으로 현재 사용자에 대해 컨텍스트가 저장되는지 여부 및 위치에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31536-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="31536-113">이 설정은 현재 세션에서 활성화된 설정과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31536-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="31536-114">위의 예제에서는 자동 저장 기능이 사용하도록 설정되고 데이터가 기본 위치에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="31536-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="31536-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31536-115">PARAMETERS</span></span>

### <span data-ttu-id="31536-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31536-116">-DefaultProfile</span></span>
<span data-ttu-id="31536-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="31536-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31536-118">-Scope</span><span class="sxs-lookup"><span data-stu-id="31536-118">-Scope</span></span>
<span data-ttu-id="31536-119">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="31536-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31536-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31536-120">CommonParameters</span></span>
<span data-ttu-id="31536-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31536-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31536-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="31536-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31536-123">입력</span><span class="sxs-lookup"><span data-stu-id="31536-123">INPUTS</span></span>

### <span data-ttu-id="31536-124">없음</span><span class="sxs-lookup"><span data-stu-id="31536-124">None</span></span>

## <span data-ttu-id="31536-125">출력</span><span class="sxs-lookup"><span data-stu-id="31536-125">OUTPUTS</span></span>

### <span data-ttu-id="31536-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="31536-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="31536-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31536-127">NOTES</span></span>

## <span data-ttu-id="31536-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31536-128">RELATED LINKS</span></span>
