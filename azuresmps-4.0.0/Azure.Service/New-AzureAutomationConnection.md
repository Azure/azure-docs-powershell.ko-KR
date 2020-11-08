---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B7E71C5C-6329-475B-993C-A839FFEF8F98
online version: ''
schema: 2.0.0
ms.openlocfilehash: cef5d19cdb954e98fe0e97cc0042bfaf91505c0c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046220"
---
# <span data-ttu-id="8cf1a-101">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="8cf1a-101">New-AzureAutomationConnection</span></span>

## <span data-ttu-id="8cf1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cf1a-102">SYNOPSIS</span></span>

<span data-ttu-id="8cf1a-103">자동화에 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-103">Creates a connection in Automation.</span></span>

## <span data-ttu-id="8cf1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8cf1a-104">SYNTAX</span></span>

```
New-AzureAutomationConnection -Name <String> -ConnectionTypeName <String> -ConnectionFieldValues <IDictionary>
 [-Description <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8cf1a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8cf1a-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="8cf1a-106">**새로운-AzureAutomationConnection** Cmdlet은 Microsoft Azure 자동화에 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-106">The **New-AzureAutomationConnection** cmdlet creates a connection in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="8cf1a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8cf1a-107">EXAMPLES</span></span>

## <span data-ttu-id="8cf1a-108">변수</span><span class="sxs-lookup"><span data-stu-id="8cf1a-108">PARAMETERS</span></span>

### <span data-ttu-id="8cf1a-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8cf1a-109">-AutomationAccountName</span></span>
<span data-ttu-id="8cf1a-110">연결이 저장 되는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-110">Specifies the name of the Automation account the connection will be stored in.</span></span>

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

### <span data-ttu-id="8cf1a-111">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="8cf1a-111">-ConnectionFieldValues</span></span>
<span data-ttu-id="8cf1a-112">키/값 쌍이 포함 된 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-112">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="8cf1a-113">키는 지정 된 연결 형식에 대 한 연결 필드를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-113">The keys represent the connection fields on the specified connection type.</span></span>
<span data-ttu-id="8cf1a-114">값은 연결 인스턴스의 각 연결 필드에 대해 저장할 특정 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-114">The values represent the specific values to store for each connection field for the connection instance.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf1a-115">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="8cf1a-115">-ConnectionTypeName</span></span>
<span data-ttu-id="8cf1a-116">연결 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-116">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="8cf1a-117">-설명</span><span class="sxs-lookup"><span data-stu-id="8cf1a-117">-Description</span></span>
<span data-ttu-id="8cf1a-118">자격 증명에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-118">Specifies a description for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf1a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8cf1a-119">-Name</span></span>
<span data-ttu-id="8cf1a-120">연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-120">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="8cf1a-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="8cf1a-121">-Profile</span></span>
<span data-ttu-id="8cf1a-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8cf1a-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8cf1a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf1a-124">CommonParameters</span></span>
<span data-ttu-id="8cf1a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf1a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf1a-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf1a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf1a-127">입력</span><span class="sxs-lookup"><span data-stu-id="8cf1a-127">INPUTS</span></span>

## <span data-ttu-id="8cf1a-128">출력</span><span class="sxs-lookup"><span data-stu-id="8cf1a-128">OUTPUTS</span></span>

### <span data-ttu-id="8cf1a-129">Microsoft. Azure. 연결</span><span class="sxs-lookup"><span data-stu-id="8cf1a-129">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="8cf1a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="8cf1a-130">NOTES</span></span>

## <span data-ttu-id="8cf1a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cf1a-131">RELATED LINKS</span></span>

[<span data-ttu-id="8cf1a-132">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="8cf1a-132">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="8cf1a-133">-AzureAutomationConnection 제거</span><span class="sxs-lookup"><span data-stu-id="8cf1a-133">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="8cf1a-134">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="8cf1a-134">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


