---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
ms.openlocfilehash: 60120e66596830e018351ceb492a36cd1ad1032d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530722"
---
# <span data-ttu-id="8d351-101">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="8d351-101">Get-AzureRmContextAutosaveSetting</span></span>

## <span data-ttu-id="8d351-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d351-102">SYNOPSIS</span></span>
<span data-ttu-id="8d351-103">컨텍스트 자동 저장 기능에 대 한 메타 데이터 표시 (context terh 포함) aved 및 저장 된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8d351-103">Display metadata about the context autosave feature, including whterh the context is automaticallys aved, and where saved context and credential information cna be found.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d351-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d351-104">SYNTAX</span></span>

```
Get-AzureRmContextAutosaveSetting [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d351-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8d351-105">DESCRIPTION</span></span>
<span data-ttu-id="8d351-106">컨텍스트가 자동으로 저장 되는지 여부와 저장 된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함 하 여 컨텍스트 자동 저장 기능에 대 한 메타 데이터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d351-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="8d351-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8d351-107">EXAMPLES</span></span>

### <span data-ttu-id="8d351-108">현재 세션에 대 한 컨텍스트 저장 메타 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="8d351-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="8d351-109">컨텍스트 저장 여부에 대 한 세부 정보를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d351-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="8d351-110">위의 예제에서는 자동 저장 기능을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8d351-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="8d351-111">현재 사용자의 컨텍스트 저장 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d351-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="8d351-112">현재 사용자에 대해 컨텍스트가 기본적으로 저장 되는지 여부에 대 한 세부 정보를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d351-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="8d351-113">이는 현재 세션에서 활성 상태인 설정과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d351-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="8d351-114">위의 예제에서는 자동 저장 기능을 사용 하도록 설정 하 고 데이터를 기본 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d351-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="8d351-115">변수</span><span class="sxs-lookup"><span data-stu-id="8d351-115">PARAMETERS</span></span>

### <span data-ttu-id="8d351-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d351-116">-DefaultProfile</span></span>
<span data-ttu-id="8d351-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8d351-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d351-118">-범위</span><span class="sxs-lookup"><span data-stu-id="8d351-118">-Scope</span></span>
<span data-ttu-id="8d351-119">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d351-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="8d351-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d351-120">CommonParameters</span></span>
<span data-ttu-id="8d351-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d351-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d351-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d351-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d351-123">입력</span><span class="sxs-lookup"><span data-stu-id="8d351-123">INPUTS</span></span>

### <span data-ttu-id="8d351-124">않아야</span><span class="sxs-lookup"><span data-stu-id="8d351-124">None</span></span>

## <span data-ttu-id="8d351-125">출력</span><span class="sxs-lookup"><span data-stu-id="8d351-125">OUTPUTS</span></span>

### <span data-ttu-id="8d351-126">Microsoft. Azure. Common. 인증. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="8d351-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="8d351-127">현재 사용자에 대해 자동 저장이 사용 되는지 여부와 컨텍스트 및 자격 증명 파일이 저장 되는 위치를 비롯 하 여 현재 자동 저장 설정에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="8d351-127">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="8d351-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8d351-128">NOTES</span></span>

## <span data-ttu-id="8d351-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d351-129">RELATED LINKS</span></span>

