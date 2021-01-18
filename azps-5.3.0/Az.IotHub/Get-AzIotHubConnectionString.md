---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495384"
---
# <span data-ttu-id="4030b-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="4030b-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="4030b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4030b-102">SYNOPSIS</span></span>
<span data-ttu-id="4030b-103">IotHub 연결스트링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4030b-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="4030b-104">구문</span><span class="sxs-lookup"><span data-stu-id="4030b-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4030b-105">설명</span><span class="sxs-lookup"><span data-stu-id="4030b-105">DESCRIPTION</span></span>
<span data-ttu-id="4030b-106">IotHub 연결스트링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4030b-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="4030b-107">모든 키에 대한 connectionstrings를 얻거나 특정 키 이름으로 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4030b-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="4030b-108">예제</span><span class="sxs-lookup"><span data-stu-id="4030b-108">EXAMPLES</span></span>

### <span data-ttu-id="4030b-109">예제 1 모든 IotHub 연결스트링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4030b-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4030b-110">"myiothub"라는 iothub에 대한 모든 키에 대한 connectionstrings를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4030b-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="4030b-111">예제 2 특정 키에 대한 IotHub 연결스트링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4030b-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="4030b-112">"myiothub"라는 iothub에 대한 "mykey"라는 키에 대한 connectionstrings를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4030b-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="4030b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4030b-113">PARAMETERS</span></span>

### <span data-ttu-id="4030b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4030b-114">-DefaultProfile</span></span>
<span data-ttu-id="4030b-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4030b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4030b-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4030b-116">-KeyName</span></span>
<span data-ttu-id="4030b-117">키의 이름</span><span class="sxs-lookup"><span data-stu-id="4030b-117">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4030b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4030b-118">-Name</span></span>
<span data-ttu-id="4030b-119">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="4030b-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="4030b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4030b-120">-ResourceGroupName</span></span>
<span data-ttu-id="4030b-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4030b-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4030b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4030b-122">CommonParameters</span></span>
<span data-ttu-id="4030b-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4030b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4030b-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4030b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4030b-125">입력</span><span class="sxs-lookup"><span data-stu-id="4030b-125">INPUTS</span></span>

### <span data-ttu-id="4030b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4030b-126">System.String</span></span>

## <span data-ttu-id="4030b-127">출력</span><span class="sxs-lookup"><span data-stu-id="4030b-127">OUTPUTS</span></span>

### <span data-ttu-id="4030b-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4030b-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="4030b-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4030b-129">NOTES</span></span>

## <span data-ttu-id="4030b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4030b-130">RELATED LINKS</span></span>
