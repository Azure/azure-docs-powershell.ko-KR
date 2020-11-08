---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 24348c44ef9b529507c50a689f181739d1474e22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218681"
---
# <span data-ttu-id="799ef-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="799ef-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="799ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="799ef-102">SYNOPSIS</span></span>
<span data-ttu-id="799ef-103">Azure eventhub에 대 한 SAS 토큰을 생성 합니다. 네임 스페이스/eventhub의 권한 부여 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="799ef-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="799ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="799ef-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="799ef-105">설명은</span><span class="sxs-lookup"><span data-stu-id="799ef-105">DESCRIPTION</span></span>
<span data-ttu-id="799ef-106">New-AzEventHubAuthorizationRuleSASToken cmdlet이 Azure Eventhub Namesapce 또는 Azure Eventhub에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="799ef-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="799ef-107">예제의</span><span class="sxs-lookup"><span data-stu-id="799ef-107">EXAMPLES</span></span>

### <span data-ttu-id="799ef-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="799ef-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="799ef-109">시작 및 만료 시간이 포함 된 네임 스페이스에 대해 지정 된 authorixation 규칙에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="799ef-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="799ef-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="799ef-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="799ef-111">만료 시간과 함께 네임 스페이스에 대해 지정 된 authorixation 규칙에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="799ef-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="799ef-112">변수</span><span class="sxs-lookup"><span data-stu-id="799ef-112">PARAMETERS</span></span>

### <span data-ttu-id="799ef-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="799ef-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="799ef-114">기관 \ 조직 규칙의 팔 ResourceId</span><span class="sxs-lookup"><span data-stu-id="799ef-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="799ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="799ef-115">-DefaultProfile</span></span>
<span data-ttu-id="799ef-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="799ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="799ef-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="799ef-117">-ExpiryTime</span></span>
<span data-ttu-id="799ef-118">만료 시간</span><span class="sxs-lookup"><span data-stu-id="799ef-118">Expiry Time</span></span>

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

### <span data-ttu-id="799ef-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="799ef-119">-KeyType</span></span>
<span data-ttu-id="799ef-120">키 유형</span><span class="sxs-lookup"><span data-stu-id="799ef-120">Key Type</span></span>

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

### <span data-ttu-id="799ef-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="799ef-121">-StartTime</span></span>
<span data-ttu-id="799ef-122">시작 시간</span><span class="sxs-lookup"><span data-stu-id="799ef-122">Start Time</span></span>

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

### <span data-ttu-id="799ef-123">-확인</span><span class="sxs-lookup"><span data-stu-id="799ef-123">-Confirm</span></span>
<span data-ttu-id="799ef-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="799ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="799ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="799ef-125">-WhatIf</span></span>
<span data-ttu-id="799ef-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="799ef-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="799ef-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="799ef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="799ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="799ef-128">CommonParameters</span></span>
<span data-ttu-id="799ef-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="799ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="799ef-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="799ef-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="799ef-131">입력</span><span class="sxs-lookup"><span data-stu-id="799ef-131">INPUTS</span></span>

### <span data-ttu-id="799ef-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="799ef-132">System.String</span></span>

### <span data-ttu-id="799ef-133">시스템 Null 허용 ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="799ef-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="799ef-134">출력</span><span class="sxs-lookup"><span data-stu-id="799ef-134">OUTPUTS</span></span>

### <span data-ttu-id="799ef-135">Microsoft. \*. m a m. 모델. Pssharedaccess서명 특성</span><span class="sxs-lookup"><span data-stu-id="799ef-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="799ef-136">상속자</span><span class="sxs-lookup"><span data-stu-id="799ef-136">NOTES</span></span>

## <span data-ttu-id="799ef-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="799ef-137">RELATED LINKS</span></span>
