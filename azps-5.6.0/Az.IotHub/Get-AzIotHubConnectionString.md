---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: ba5ab4214de0272338bac61cdf1bbabc9507a9ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988115"
---
# <span data-ttu-id="19a00-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="19a00-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="19a00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19a00-102">SYNOPSIS</span></span>
<span data-ttu-id="19a00-103">IotHub 연결스트링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19a00-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="19a00-104">구문</span><span class="sxs-lookup"><span data-stu-id="19a00-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19a00-105">설명</span><span class="sxs-lookup"><span data-stu-id="19a00-105">DESCRIPTION</span></span>
<span data-ttu-id="19a00-106">IotHub 연결스트링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19a00-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="19a00-107">모든 키에 대한 연결스트링을 얻거나 특정 키 이름으로 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19a00-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="19a00-108">예제</span><span class="sxs-lookup"><span data-stu-id="19a00-108">EXAMPLES</span></span>

### <span data-ttu-id="19a00-109">예제 1 모든 IotHub 연결스트링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19a00-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="19a00-110">"myiothub"라는 iothub의 모든 키에 대한 연결스트링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19a00-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="19a00-111">예제 2 특정 키에 대한 IotHub 연결스트링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19a00-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="19a00-112">"myiothub"라는 iothub의 "mykey"라는 키에 대한 연결스트링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19a00-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="19a00-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="19a00-113">PARAMETERS</span></span>

### <span data-ttu-id="19a00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19a00-114">-DefaultProfile</span></span>
<span data-ttu-id="19a00-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="19a00-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19a00-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="19a00-116">-KeyName</span></span>
<span data-ttu-id="19a00-117">키의 이름</span><span class="sxs-lookup"><span data-stu-id="19a00-117">Name of the Key</span></span>

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

### <span data-ttu-id="19a00-118">-Name</span><span class="sxs-lookup"><span data-stu-id="19a00-118">-Name</span></span>
<span data-ttu-id="19a00-119">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="19a00-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="19a00-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19a00-120">-ResourceGroupName</span></span>
<span data-ttu-id="19a00-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="19a00-121">Resource Group Name</span></span>

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

### <span data-ttu-id="19a00-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a00-122">CommonParameters</span></span>
<span data-ttu-id="19a00-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19a00-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a00-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="19a00-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a00-125">입력</span><span class="sxs-lookup"><span data-stu-id="19a00-125">INPUTS</span></span>

### <span data-ttu-id="19a00-126">System.String</span><span class="sxs-lookup"><span data-stu-id="19a00-126">System.String</span></span>

## <span data-ttu-id="19a00-127">출력</span><span class="sxs-lookup"><span data-stu-id="19a00-127">OUTPUTS</span></span>

### <span data-ttu-id="19a00-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="19a00-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="19a00-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19a00-129">NOTES</span></span>

## <span data-ttu-id="19a00-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19a00-130">RELATED LINKS</span></span>
