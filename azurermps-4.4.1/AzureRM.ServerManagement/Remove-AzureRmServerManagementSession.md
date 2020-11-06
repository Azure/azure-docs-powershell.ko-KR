---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: d34678b6ff7996eabf807c92a84d647af15f6a71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530672"
---
# <span data-ttu-id="2cc8c-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="2cc8c-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="2cc8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cc8c-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc8c-103">서버 관리 세션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cc8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2cc8c-104">SYNTAX</span></span>

### <span data-ttu-id="2cc8c-105">ByName</span><span class="sxs-lookup"><span data-stu-id="2cc8c-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc8c-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="2cc8c-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cc8c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2cc8c-107">DESCRIPTION</span></span>
<span data-ttu-id="2cc8c-108">**AzureRmServerManagementSession** Cmdlet은 Azure 서버 관리 세션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="2cc8c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2cc8c-109">EXAMPLES</span></span>

## <span data-ttu-id="2cc8c-110">변수</span><span class="sxs-lookup"><span data-stu-id="2cc8c-110">PARAMETERS</span></span>

### <span data-ttu-id="2cc8c-111">-NodeName</span><span class="sxs-lookup"><span data-stu-id="2cc8c-111">-NodeName</span></span>
<span data-ttu-id="2cc8c-112">이 cmdlet이 세션을 제거 하는 노드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-112">Specifies the name of the node on which this cmdlet removes the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc8c-113">-ResourceGroupName</span></span>
<span data-ttu-id="2cc8c-114">세션이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-114">Specifies the name of the resource group that the session belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-115">-세션</span><span class="sxs-lookup"><span data-stu-id="2cc8c-115">-Session</span></span>
<span data-ttu-id="2cc8c-116">이 cmdlet이 제거 하는 세션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-116">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="2cc8c-117">이 매개 변수는 *ResourceGroupName* , *NodeName* 및 *세션 이름* 매개 변수 대신 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-117">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-118">-세션 이름</span><span class="sxs-lookup"><span data-stu-id="2cc8c-118">-SessionName</span></span>
<span data-ttu-id="2cc8c-119">이 cmdlet이 제거 하는 세션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-119">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc8c-120">-DefaultProfile</span></span>
<span data-ttu-id="2cc8c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cc8c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc8c-122">CommonParameters</span></span>
<span data-ttu-id="2cc8c-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc8c-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc8c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc8c-125">입력</span><span class="sxs-lookup"><span data-stu-id="2cc8c-125">INPUTS</span></span>

### <span data-ttu-id="2cc8c-126">세션만</span><span class="sxs-lookup"><span data-stu-id="2cc8c-126">Session</span></span>
<span data-ttu-id="2cc8c-127">' Session ' 매개 변수는 파이프라인에서 ' Session ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="2cc8c-128">출력</span><span class="sxs-lookup"><span data-stu-id="2cc8c-128">OUTPUTS</span></span>

## <span data-ttu-id="2cc8c-129">상속자</span><span class="sxs-lookup"><span data-stu-id="2cc8c-129">NOTES</span></span>

## <span data-ttu-id="2cc8c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2cc8c-130">RELATED LINKS</span></span>

[<span data-ttu-id="2cc8c-131">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="2cc8c-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="2cc8c-132">새로운 AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="2cc8c-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)


