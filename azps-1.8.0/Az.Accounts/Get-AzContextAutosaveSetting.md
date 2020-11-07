---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: a6361fabaa05d99b35874ce0de388ed0fc1bdfa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689263"
---
# <span data-ttu-id="ffb95-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="ffb95-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="ffb95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffb95-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb95-103">컨텍스트가 자동으로 저장 되는지 여부와 저장 된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함 하 여 컨텍스트 자동 저장 기능에 대 한 메타 데이터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb95-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="ffb95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ffb95-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ffb95-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ffb95-105">DESCRIPTION</span></span>
<span data-ttu-id="ffb95-106">컨텍스트가 자동으로 저장 되는지 여부와 저장 된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함 하 여 컨텍스트 자동 저장 기능에 대 한 메타 데이터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb95-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="ffb95-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ffb95-107">EXAMPLES</span></span>

### <span data-ttu-id="ffb95-108">현재 세션에 대 한 컨텍스트 저장 메타 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="ffb95-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="ffb95-109">컨텍스트 저장 여부에 대 한 세부 정보를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffb95-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="ffb95-110">위의 예제에서는 자동 저장 기능을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ffb95-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="ffb95-111">현재 사용자의 컨텍스트 저장 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ffb95-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="ffb95-112">현재 사용자에 대해 컨텍스트가 기본적으로 저장 되는지 여부에 대 한 세부 정보를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffb95-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="ffb95-113">이는 현재 세션에서 활성 상태인 설정과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffb95-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="ffb95-114">위의 예제에서는 자동 저장 기능을 사용 하도록 설정 하 고 데이터를 기본 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb95-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="ffb95-115">변수</span><span class="sxs-lookup"><span data-stu-id="ffb95-115">PARAMETERS</span></span>

### <span data-ttu-id="ffb95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb95-116">-DefaultProfile</span></span>
<span data-ttu-id="ffb95-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ffb95-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffb95-118">-범위</span><span class="sxs-lookup"><span data-stu-id="ffb95-118">-Scope</span></span>
<span data-ttu-id="ffb95-119">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb95-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ffb95-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb95-120">CommonParameters</span></span>
<span data-ttu-id="ffb95-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb95-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb95-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffb95-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb95-123">입력</span><span class="sxs-lookup"><span data-stu-id="ffb95-123">INPUTS</span></span>

### <span data-ttu-id="ffb95-124">않아야</span><span class="sxs-lookup"><span data-stu-id="ffb95-124">None</span></span>

## <span data-ttu-id="ffb95-125">출력</span><span class="sxs-lookup"><span data-stu-id="ffb95-125">OUTPUTS</span></span>

### <span data-ttu-id="ffb95-126">Microsoft. Azure. Common. 인증. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="ffb95-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="ffb95-127">상속자</span><span class="sxs-lookup"><span data-stu-id="ffb95-127">NOTES</span></span>

## <span data-ttu-id="ffb95-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffb95-128">RELATED LINKS</span></span>
