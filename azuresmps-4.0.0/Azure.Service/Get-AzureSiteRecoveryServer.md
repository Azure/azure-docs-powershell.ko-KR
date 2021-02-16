---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79b61501a56913fedb2a003d7aea1a041bfab4d5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412285"
---
# <span data-ttu-id="0f5a3-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="0f5a3-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="0f5a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5a3-103">Site Recovery 자격 증명 모음을 등록한 Site Recovery 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a3-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="0f5a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="0f5a3-104">SYNTAX</span></span>

### <span data-ttu-id="0f5a3-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="0f5a3-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0f5a3-106">ById</span><span class="sxs-lookup"><span data-stu-id="0f5a3-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0f5a3-107">ByName</span><span class="sxs-lookup"><span data-stu-id="0f5a3-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0f5a3-108">설명</span><span class="sxs-lookup"><span data-stu-id="0f5a3-108">DESCRIPTION</span></span>
<span data-ttu-id="0f5a3-109">**Get-AzureSiteRecoveryServer** cmdlet은 현재 Site Recovery 자격 증명 모음에 등록된 Azure Site Recovery 서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a3-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="0f5a3-110">예제</span><span class="sxs-lookup"><span data-stu-id="0f5a3-110">EXAMPLES</span></span>

### <span data-ttu-id="0f5a3-111">예제 1: Site Recovery 서버에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="0f5a3-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="0f5a3-112">이 명령은 Azure Site Recovery 서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a3-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="0f5a3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f5a3-113">PARAMETERS</span></span>

### <span data-ttu-id="0f5a3-114">-Id</span><span class="sxs-lookup"><span data-stu-id="0f5a3-114">-Id</span></span>
<span data-ttu-id="0f5a3-115">서버의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a3-115">Specifies the ID of a server.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f5a3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0f5a3-116">-Name</span></span>
<span data-ttu-id="0f5a3-117">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a3-117">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f5a3-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="0f5a3-118">-Profile</span></span>
<span data-ttu-id="0f5a3-119">이 cmdlet이 읽을 Azure 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a3-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f5a3-120">프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a3-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f5a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5a3-121">CommonParameters</span></span>
<span data-ttu-id="0f5a3-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5a3-123">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0f5a3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5a3-124">입력</span><span class="sxs-lookup"><span data-stu-id="0f5a3-124">INPUTS</span></span>

## <span data-ttu-id="0f5a3-125">출력</span><span class="sxs-lookup"><span data-stu-id="0f5a3-125">OUTPUTS</span></span>

## <span data-ttu-id="0f5a3-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0f5a3-126">NOTES</span></span>

## <span data-ttu-id="0f5a3-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f5a3-127">RELATED LINKS</span></span>




