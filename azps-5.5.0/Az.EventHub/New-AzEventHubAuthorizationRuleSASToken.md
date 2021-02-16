---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 24348c44ef9b529507c50a689f181739d1474e22
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194388"
---
# <span data-ttu-id="e35f7-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e35f7-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="e35f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e35f7-102">SYNOPSIS</span></span>
<span data-ttu-id="e35f7-103">네임스페이스/eventhub의 Azure eventhub 권한 부여 규칙에 대한 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e35f7-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="e35f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="e35f7-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e35f7-105">설명</span><span class="sxs-lookup"><span data-stu-id="e35f7-105">DESCRIPTION</span></span>
<span data-ttu-id="e35f7-106">이 New-AzEventHubAuthorizationRuleSASToken cmdlet은 Azure Eventhub 네임스페이스 또는 Azure Eventhub에 대한 SAS(공유 액세스 서명) 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e35f7-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="e35f7-107">예제</span><span class="sxs-lookup"><span data-stu-id="e35f7-107">EXAMPLES</span></span>

### <span data-ttu-id="e35f7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e35f7-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="e35f7-109">시작 및 만료 시간이 있는 네임스페이스에 대해 주어진 승인 규칙에 대한 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e35f7-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="e35f7-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="e35f7-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="e35f7-111">만료 시간이 있는 네임스페이스에 대해 주어진 승인 규칙에 대한 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e35f7-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="e35f7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e35f7-112">PARAMETERS</span></span>

### <span data-ttu-id="e35f7-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="e35f7-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="e35f7-114">ARM 규칙의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="e35f7-114">ARM ResourceId of the Authoraization Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35f7-115">-DefaultProfile</span></span>
<span data-ttu-id="e35f7-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e35f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e35f7-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e35f7-117">-ExpiryTime</span></span>
<span data-ttu-id="e35f7-118">만료 시간</span><span class="sxs-lookup"><span data-stu-id="e35f7-118">Expiry Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35f7-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e35f7-119">-KeyType</span></span>
<span data-ttu-id="e35f7-120">키 유형</span><span class="sxs-lookup"><span data-stu-id="e35f7-120">Key Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35f7-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e35f7-121">-StartTime</span></span>
<span data-ttu-id="e35f7-122">시작 시간</span><span class="sxs-lookup"><span data-stu-id="e35f7-122">Start Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35f7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e35f7-123">-Confirm</span></span>
<span data-ttu-id="e35f7-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e35f7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35f7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e35f7-125">-WhatIf</span></span>
<span data-ttu-id="e35f7-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e35f7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e35f7-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e35f7-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35f7-128">CommonParameters</span></span>
<span data-ttu-id="e35f7-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e35f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e35f7-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e35f7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35f7-131">입력</span><span class="sxs-lookup"><span data-stu-id="e35f7-131">INPUTS</span></span>

### <span data-ttu-id="e35f7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e35f7-132">System.String</span></span>

### <span data-ttu-id="e35f7-133">System.Nullable'1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e35f7-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e35f7-134">출력</span><span class="sxs-lookup"><span data-stu-id="e35f7-134">OUTPUTS</span></span>

### <span data-ttu-id="e35f7-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="e35f7-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="e35f7-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e35f7-136">NOTES</span></span>

## <span data-ttu-id="e35f7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e35f7-137">RELATED LINKS</span></span>
