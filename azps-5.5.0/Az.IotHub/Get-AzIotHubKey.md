---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185692"
---
# <span data-ttu-id="66182-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="66182-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="66182-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66182-102">SYNOPSIS</span></span>
<span data-ttu-id="66182-103">IotHub 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66182-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="66182-104">구문</span><span class="sxs-lookup"><span data-stu-id="66182-104">SYNTAX</span></span>

### <span data-ttu-id="66182-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="66182-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66182-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="66182-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66182-107">설명</span><span class="sxs-lookup"><span data-stu-id="66182-107">DESCRIPTION</span></span>
<span data-ttu-id="66182-108">IotHub 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66182-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="66182-109">모든 키를 나열하거나 특정 키 이름으로 목록을 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66182-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="66182-110">예제</span><span class="sxs-lookup"><span data-stu-id="66182-110">EXAMPLES</span></span>

### <span data-ttu-id="66182-111">예제 1 모든 키 얻기</span><span class="sxs-lookup"><span data-stu-id="66182-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="66182-112">"myiothub"라는 IotHub에 대한 모든 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66182-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="66182-113">예제 2 특정 키에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="66182-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="66182-114">"myiothub"라는 IotHub에 대한 "iothubowner"라는 키에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66182-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="66182-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66182-115">PARAMETERS</span></span>

### <span data-ttu-id="66182-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66182-116">-DefaultProfile</span></span>
<span data-ttu-id="66182-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="66182-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66182-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="66182-118">-HubId</span></span>
<span data-ttu-id="66182-119">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="66182-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="66182-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="66182-120">-KeyName</span></span>
<span data-ttu-id="66182-121">키의 이름</span><span class="sxs-lookup"><span data-stu-id="66182-121">Name of the Key</span></span>

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

### <span data-ttu-id="66182-122">-Name</span><span class="sxs-lookup"><span data-stu-id="66182-122">-Name</span></span>
<span data-ttu-id="66182-123">IoT Hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66182-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="66182-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66182-124">-ResourceGroupName</span></span>
<span data-ttu-id="66182-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="66182-125">Resource Group Name</span></span>

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

### <span data-ttu-id="66182-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66182-126">CommonParameters</span></span>
<span data-ttu-id="66182-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66182-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66182-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66182-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66182-129">입력</span><span class="sxs-lookup"><span data-stu-id="66182-129">INPUTS</span></span>

### <span data-ttu-id="66182-130">System.String</span><span class="sxs-lookup"><span data-stu-id="66182-130">System.String</span></span>

## <span data-ttu-id="66182-131">출력</span><span class="sxs-lookup"><span data-stu-id="66182-131">OUTPUTS</span></span>

### <span data-ttu-id="66182-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="66182-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="66182-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66182-133">NOTES</span></span>

## <span data-ttu-id="66182-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66182-134">RELATED LINKS</span></span>
