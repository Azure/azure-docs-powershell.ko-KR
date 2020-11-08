---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046370"
---
# <span data-ttu-id="b3b4d-101">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b3b4d-101">Get-AzureAutomationConnection</span></span>

## <span data-ttu-id="b3b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3b4d-102">SYNOPSIS</span></span>

<span data-ttu-id="b3b4d-103">Azure Automation 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-103">Gets an Azure Automation connection.</span></span>

## <span data-ttu-id="b3b4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3b4d-104">SYNTAX</span></span>

### <span data-ttu-id="b3b4d-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="b3b4d-105">ByAll (Default)</span></span>
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b3b4d-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="b3b4d-106">ByConnectionName</span></span>
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3b4d-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="b3b4d-107">ByConnectionTypeName</span></span>
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b3b4d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b3b4d-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b3b4d-109">**Get-AzureAutomationConnection** cmdlet은 하나 이상의 Microsoft Azure Automation 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-109">The **Get-AzureAutomationConnection** cmdlet gets one or more Microsoft Azure Automation connections.</span></span>
<span data-ttu-id="b3b4d-110">기본적으로 모든 연결이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-110">By default, all connections are returned.</span></span>
<span data-ttu-id="b3b4d-111">특정 연결을 얻으려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-111">To get a specific connection, specify its name.</span></span>
<span data-ttu-id="b3b4d-112">특정 유형의 모든 연결을 얻으려면 연결 형식 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-112">To get all connections of a certain type, specify the connection type name.</span></span>

## <span data-ttu-id="b3b4d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b3b4d-113">EXAMPLES</span></span>

### <span data-ttu-id="b3b4d-114">예제 1: 모든 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="b3b4d-114">Example 1: Get all connections</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

<span data-ttu-id="b3b4d-115">이 명령은 Contoso17 이라는 자동화 계정에 있는 모든 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-115">This command gets all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b3b4d-116">예제 2: 형식의 모든 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="b3b4d-116">Example 2: Get all connections of a type</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

<span data-ttu-id="b3b4d-117">이 명령은 Contoso17 이라는 자동화 계정에 있는 모든 Azure 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-117">This command gets all Azure connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b3b4d-118">예제 3: 연결 하기</span><span class="sxs-lookup"><span data-stu-id="b3b4d-118">Example 3: Get a connection</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

<span data-ttu-id="b3b4d-119">이 명령은 MyConnection 이라는 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-119">This command gets the connection named MyConnection.</span></span>

## <span data-ttu-id="b3b4d-120">변수</span><span class="sxs-lookup"><span data-stu-id="b3b4d-120">PARAMETERS</span></span>

### <span data-ttu-id="b3b4d-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b3b4d-121">-AutomationAccountName</span></span>
<span data-ttu-id="b3b4d-122">검색할 연결이 있는 automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-122">Specifies the name of the automation account with the connection to retrieve.</span></span>

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

### <span data-ttu-id="b3b4d-123">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="b3b4d-123">-ConnectionTypeName</span></span>
<span data-ttu-id="b3b4d-124">검색할 연결의 연결 형식 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-124">Specifies the name of a connection type for the connections to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b4d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="b3b4d-125">-Name</span></span>
<span data-ttu-id="b3b4d-126">검색할 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-126">Specifies the name of a connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b4d-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="b3b4d-127">-Profile</span></span>
<span data-ttu-id="b3b4d-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b3b4d-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b3b4d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b4d-130">CommonParameters</span></span>
<span data-ttu-id="b3b4d-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b4d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b4d-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3b4d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b4d-133">입력</span><span class="sxs-lookup"><span data-stu-id="b3b4d-133">INPUTS</span></span>

## <span data-ttu-id="b3b4d-134">출력</span><span class="sxs-lookup"><span data-stu-id="b3b4d-134">OUTPUTS</span></span>

### <span data-ttu-id="b3b4d-135">Microsoft. Azure. 연결</span><span class="sxs-lookup"><span data-stu-id="b3b4d-135">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="b3b4d-136">상속자</span><span class="sxs-lookup"><span data-stu-id="b3b4d-136">NOTES</span></span>

## <span data-ttu-id="b3b4d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3b4d-137">RELATED LINKS</span></span>

[<span data-ttu-id="b3b4d-138">새-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b3b4d-138">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="b3b4d-139">-AzureAutomationConnection 제거</span><span class="sxs-lookup"><span data-stu-id="b3b4d-139">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="b3b4d-140">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="b3b4d-140">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


