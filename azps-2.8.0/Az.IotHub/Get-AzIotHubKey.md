---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: c38965a99dfc152f76e606c05802009b9b14faf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689738"
---
# <span data-ttu-id="6975f-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="6975f-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="6975f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6975f-102">SYNOPSIS</span></span>
<span data-ttu-id="6975f-103">IotHub 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6975f-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="6975f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6975f-104">SYNTAX</span></span>

### <span data-ttu-id="6975f-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6975f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6975f-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6975f-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6975f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6975f-107">DESCRIPTION</span></span>
<span data-ttu-id="6975f-108">IotHub 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6975f-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="6975f-109">모든 키 목록을 표시 하거나 특정 키 이름으로 목록을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6975f-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="6975f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6975f-110">EXAMPLES</span></span>

### <span data-ttu-id="6975f-111">예제 1 모든 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="6975f-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="6975f-112">"Myiothub" IotHub의 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6975f-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="6975f-113">예제 2 특정 키에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="6975f-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="6975f-114">"Myiothub" 이라는 IotHub에 대 한 "iothubowner" 키에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6975f-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="6975f-115">변수</span><span class="sxs-lookup"><span data-stu-id="6975f-115">PARAMETERS</span></span>

### <span data-ttu-id="6975f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6975f-116">-DefaultProfile</span></span>
<span data-ttu-id="6975f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6975f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6975f-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="6975f-118">-HubId</span></span>
<span data-ttu-id="6975f-119">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="6975f-119">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6975f-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6975f-120">-KeyName</span></span>
<span data-ttu-id="6975f-121">키 이름</span><span class="sxs-lookup"><span data-stu-id="6975f-121">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6975f-122">-이름</span><span class="sxs-lookup"><span data-stu-id="6975f-122">-Name</span></span>
<span data-ttu-id="6975f-123">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6975f-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6975f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6975f-124">-ResourceGroupName</span></span>
<span data-ttu-id="6975f-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6975f-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6975f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6975f-126">CommonParameters</span></span>
<span data-ttu-id="6975f-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6975f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6975f-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6975f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6975f-129">입력</span><span class="sxs-lookup"><span data-stu-id="6975f-129">INPUTS</span></span>

### <span data-ttu-id="6975f-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6975f-130">System.String</span></span>

## <span data-ttu-id="6975f-131">출력</span><span class="sxs-lookup"><span data-stu-id="6975f-131">OUTPUTS</span></span>

### <span data-ttu-id="6975f-132">IotHub를 호출 합니다. Pssharedaccess서명 Authorizationrule</span><span class="sxs-lookup"><span data-stu-id="6975f-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="6975f-133">상속자</span><span class="sxs-lookup"><span data-stu-id="6975f-133">NOTES</span></span>

## <span data-ttu-id="6975f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6975f-134">RELATED LINKS</span></span>
