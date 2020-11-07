---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 29f9fc8847e4b8bf3ab348fcad8f312dab71fd0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875879"
---
# <span data-ttu-id="b1472-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b1472-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="b1472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1472-102">SYNOPSIS</span></span>
<span data-ttu-id="b1472-103">IotHub 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1472-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="b1472-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1472-104">SYNTAX</span></span>

### <span data-ttu-id="b1472-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b1472-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1472-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b1472-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1472-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b1472-107">DESCRIPTION</span></span>
<span data-ttu-id="b1472-108">IotHub 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1472-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="b1472-109">모든 키 목록을 표시 하거나 특정 키 이름으로 목록을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1472-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="b1472-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b1472-110">EXAMPLES</span></span>

### <span data-ttu-id="b1472-111">예제 1 모든 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1472-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b1472-112">"Myiothub" IotHub의 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1472-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="b1472-113">예제 2 특정 키에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1472-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="b1472-114">"Myiothub" 이라는 IotHub에 대 한 "iothubowner" 키에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1472-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b1472-115">변수</span><span class="sxs-lookup"><span data-stu-id="b1472-115">PARAMETERS</span></span>

### <span data-ttu-id="b1472-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1472-116">-DefaultProfile</span></span>
<span data-ttu-id="b1472-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b1472-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1472-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="b1472-118">-HubId</span></span>
<span data-ttu-id="b1472-119">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="b1472-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b1472-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b1472-120">-KeyName</span></span>
<span data-ttu-id="b1472-121">키 이름</span><span class="sxs-lookup"><span data-stu-id="b1472-121">Name of the Key</span></span>

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

### <span data-ttu-id="b1472-122">-이름</span><span class="sxs-lookup"><span data-stu-id="b1472-122">-Name</span></span>
<span data-ttu-id="b1472-123">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1472-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="b1472-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1472-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1472-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b1472-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b1472-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1472-126">CommonParameters</span></span>
<span data-ttu-id="b1472-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1472-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1472-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1472-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1472-129">입력</span><span class="sxs-lookup"><span data-stu-id="b1472-129">INPUTS</span></span>

### <span data-ttu-id="b1472-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b1472-130">System.String</span></span>

## <span data-ttu-id="b1472-131">출력</span><span class="sxs-lookup"><span data-stu-id="b1472-131">OUTPUTS</span></span>

### <span data-ttu-id="b1472-132">IotHub를 호출 합니다. Pssharedaccess서명 Authorizationrule</span><span class="sxs-lookup"><span data-stu-id="b1472-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b1472-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b1472-133">NOTES</span></span>

## <span data-ttu-id="b1472-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1472-134">RELATED LINKS</span></span>
