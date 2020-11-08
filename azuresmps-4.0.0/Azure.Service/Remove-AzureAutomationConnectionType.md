---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4370FF88-E34F-499D-AF57-53C15B4EB6E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: e55d9e54dcaa0f547d64ec58b2772a581a8ec30a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046484"
---
# <span data-ttu-id="d7d97-101">Remove-AzureAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="d7d97-101">Remove-AzureAutomationConnectionType</span></span>

## <span data-ttu-id="d7d97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7d97-102">SYNOPSIS</span></span>

<span data-ttu-id="d7d97-103">연결 형식을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7d97-103">Removes a connection type.</span></span>

## <span data-ttu-id="d7d97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7d97-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnectionType -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d7d97-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d7d97-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d7d97-106">**제거-AzureAutomationConnectionType** Cmdlet은 Azure Automation 연결 형식을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7d97-106">The **Remove-AzureAutomationConnectionType** cmdlet removes an Azure Automation connection type.</span></span>

## <span data-ttu-id="d7d97-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d7d97-107">EXAMPLES</span></span>

## <span data-ttu-id="d7d97-108">변수</span><span class="sxs-lookup"><span data-stu-id="d7d97-108">PARAMETERS</span></span>

### <span data-ttu-id="d7d97-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d7d97-109">-AutomationAccountName</span></span>
<span data-ttu-id="d7d97-110">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7d97-110">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d97-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d7d97-111">-Force</span></span>
<span data-ttu-id="d7d97-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7d97-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d7d97-113">-이름</span><span class="sxs-lookup"><span data-stu-id="d7d97-113">-Name</span></span>
<span data-ttu-id="d7d97-114">제거할 연결 유형의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7d97-114">Specifies the name of the connection type to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d97-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="d7d97-115">-Profile</span></span>
<span data-ttu-id="d7d97-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7d97-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7d97-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d7d97-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d97-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d97-118">CommonParameters</span></span>
<span data-ttu-id="d7d97-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7d97-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d97-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7d97-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d97-121">입력</span><span class="sxs-lookup"><span data-stu-id="d7d97-121">INPUTS</span></span>

## <span data-ttu-id="d7d97-122">출력</span><span class="sxs-lookup"><span data-stu-id="d7d97-122">OUTPUTS</span></span>

## <span data-ttu-id="d7d97-123">상속자</span><span class="sxs-lookup"><span data-stu-id="d7d97-123">NOTES</span></span>

## <span data-ttu-id="d7d97-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7d97-124">RELATED LINKS</span></span>

