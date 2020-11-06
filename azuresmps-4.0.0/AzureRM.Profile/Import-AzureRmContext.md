---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522683"
---
# <span data-ttu-id="80818-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="80818-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="80818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80818-102">SYNOPSIS</span></span>
<span data-ttu-id="80818-103">파일에서 Azure 인증 정보를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="80818-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="80818-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80818-104">SYNTAX</span></span>

### <span data-ttu-id="80818-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="80818-105">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="80818-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="80818-106">ProfileFromDisk</span></span>
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="80818-107">설명은</span><span class="sxs-lookup"><span data-stu-id="80818-107">DESCRIPTION</span></span>
<span data-ttu-id="80818-108">Import-AzureRmContext cmdlet은 파일에서 인증 정보를 로드 하 여 Azure 환경 및 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80818-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="80818-109">현재 세션에서 실행 하는 cmdlet은이 정보를 사용 하 여 Azure Resource Manager에 대 한 요청을 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="80818-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="80818-110">예제의</span><span class="sxs-lookup"><span data-stu-id="80818-110">EXAMPLES</span></span>

### <span data-ttu-id="80818-111">예제 1: AzureRmProfile에서 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="80818-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="80818-112">이 예제에서는 cmdlet으로 전달 되는 PSAzureProfile에서 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="80818-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="80818-113">예제 2: JSON 파일에서 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="80818-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="80818-114">이 예제에서는 cmdlet으로 전달 되는 JSON 파일에서 컨텍스트를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="80818-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span>
<span data-ttu-id="80818-115">이 JSON 파일은 가져오기-AzureRmContext에서 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80818-115">This JSON file can be created from Import-AzureRmContext.</span></span>

## <span data-ttu-id="80818-116">변수</span><span class="sxs-lookup"><span data-stu-id="80818-116">PARAMETERS</span></span>

### <span data-ttu-id="80818-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="80818-117">-AzureContext</span></span>
<span data-ttu-id="80818-118">이 cmdlet이 읽는 Azure 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80818-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="80818-119">컨텍스트를 지정 하지 않으면이 cmdlet은 로컬 기본 컨텍스트를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="80818-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80818-120">-Path</span><span class="sxs-lookup"><span data-stu-id="80818-120">-Path</span></span>
<span data-ttu-id="80818-121">Save-AzureRMContext를 사용 하 여 저장 된 컨텍스트 정보의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80818-121">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80818-122">-확인</span><span class="sxs-lookup"><span data-stu-id="80818-122">-Confirm</span></span>
<span data-ttu-id="80818-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80818-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80818-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80818-124">-WhatIf</span></span>
<span data-ttu-id="80818-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80818-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80818-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80818-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="80818-127">입력</span><span class="sxs-lookup"><span data-stu-id="80818-127">INPUTS</span></span>

### <span data-ttu-id="80818-128">AzureRMProfile (일반. 인증. 모델)</span><span class="sxs-lookup"><span data-stu-id="80818-128">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="80818-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="80818-129">System.String</span></span>

## <span data-ttu-id="80818-130">출력</span><span class="sxs-lookup"><span data-stu-id="80818-130">OUTPUTS</span></span>

### <span data-ttu-id="80818-131">Microsoft. Azure. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="80818-131">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="80818-132">상속자</span><span class="sxs-lookup"><span data-stu-id="80818-132">NOTES</span></span>

## <span data-ttu-id="80818-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80818-133">RELATED LINKS</span></span>

