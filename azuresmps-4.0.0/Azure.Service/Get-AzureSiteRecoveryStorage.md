---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 78DE0AD2-6210-4604-89A8-41915D58BD68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c40cb0fd38953ff46fa1138dc91f0b9e97ece75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045576"
---
# <span data-ttu-id="97ad1-101">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="97ad1-101">Get-AzureSiteRecoveryStorage</span></span>

## <span data-ttu-id="97ad1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="97ad1-103">자격 증명 모음의 사이트 복구 저장소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97ad1-103">Gets Site Recovery Storages for a vault.</span></span>

## <span data-ttu-id="97ad1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97ad1-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorage -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="97ad1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="97ad1-105">DESCRIPTION</span></span>
<span data-ttu-id="97ad1-106">**AzureSiteRecoveryStorage** cmdlet은 현재 Azure site recovery 자격 증명 모음에 대 한 Azure Site recovery 저장소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97ad1-106">The **Get-AzureSiteRecoveryStorage** cmdlet gets Azure Site Recovery Storages for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="97ad1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="97ad1-107">EXAMPLES</span></span>

### <span data-ttu-id="97ad1-108">예제 1: 사이트 복구 저장소 가져오기</span><span class="sxs-lookup"><span data-stu-id="97ad1-108">Example 1: Get site recovery storage</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorage -Server $Servers[0]
Name           : phase2PrimaryStorageClassification
ID             : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
FabricObjectID : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM

Name           : phase2RecoveryStorageClassification
ID             : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
FabricObjectID : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM
```

<span data-ttu-id="97ad1-109">첫 번째 명령 cmdlet은 **AzureSiteRecoveryServer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 대 한 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97ad1-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="97ad1-110">명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="97ad1-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="97ad1-111">두 번째 명령은 $Servers 배열의 첫 번째 서버에 대 한 사이트 복구 저장소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97ad1-111">The second command gets the site recovery storage for the first server in the $Servers array.</span></span>

## <span data-ttu-id="97ad1-112">변수</span><span class="sxs-lookup"><span data-stu-id="97ad1-112">PARAMETERS</span></span>

### <span data-ttu-id="97ad1-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="97ad1-113">-Profile</span></span>
<span data-ttu-id="97ad1-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97ad1-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97ad1-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="97ad1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="97ad1-116">-서버</span><span class="sxs-lookup"><span data-stu-id="97ad1-116">-Server</span></span>
<span data-ttu-id="97ad1-117">Azure Site Recovery 저장소에 대 한 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97ad1-117">Specifies a server for Azure Site Recovery Storage.</span></span>
<span data-ttu-id="97ad1-118">**Asrserver** 개체를 얻으려면 **Get-AzureSiteRecoveryServer** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="97ad1-118">To obtain an **ASRServer** object, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97ad1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ad1-119">CommonParameters</span></span>
<span data-ttu-id="97ad1-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97ad1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ad1-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97ad1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ad1-122">입력</span><span class="sxs-lookup"><span data-stu-id="97ad1-122">INPUTS</span></span>

## <span data-ttu-id="97ad1-123">출력</span><span class="sxs-lookup"><span data-stu-id="97ad1-123">OUTPUTS</span></span>

## <span data-ttu-id="97ad1-124">상속자</span><span class="sxs-lookup"><span data-stu-id="97ad1-124">NOTES</span></span>

## <span data-ttu-id="97ad1-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97ad1-125">RELATED LINKS</span></span>

[<span data-ttu-id="97ad1-126">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="97ad1-126">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


