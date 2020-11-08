---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96b51b49d76093be96eeab26417f4a70f70c4627
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045592"
---
# <span data-ttu-id="dbc96-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="dbc96-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="dbc96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc96-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc96-103">현재 자격 증명 모음의 사이트 복구에서 관리 되는 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dbc96-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="dbc96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbc96-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dbc96-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dbc96-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc96-106">**AzureSiteRecoveryNetwork** cmdlet은 현재 사이트 복구 자격 증명 모음에 대 한 Azure Site recovery 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dbc96-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="dbc96-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dbc96-107">EXAMPLES</span></span>

### <span data-ttu-id="dbc96-108">예제 1: 사이트 복구 네트워크 가져오기</span><span class="sxs-lookup"><span data-stu-id="dbc96-108">Example 1: Get site recovery networks</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

<span data-ttu-id="dbc96-109">첫 번째 명령 cmdlet은 **AzureSiteRecoveryServer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 대 한 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dbc96-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="dbc96-110">명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbc96-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="dbc96-111">두 번째 명령은 $Servers 배열의 첫 번째 서버에 대 한 사이트 복구 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dbc96-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="dbc96-112">변수</span><span class="sxs-lookup"><span data-stu-id="dbc96-112">PARAMETERS</span></span>

### <span data-ttu-id="dbc96-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="dbc96-113">-Profile</span></span>
<span data-ttu-id="dbc96-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbc96-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dbc96-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="dbc96-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dbc96-116">-서버</span><span class="sxs-lookup"><span data-stu-id="dbc96-116">-Server</span></span>
<span data-ttu-id="dbc96-117">사이트 복구 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbc96-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="dbc96-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc96-118">CommonParameters</span></span>
<span data-ttu-id="dbc96-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbc96-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc96-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbc96-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc96-121">입력</span><span class="sxs-lookup"><span data-stu-id="dbc96-121">INPUTS</span></span>

## <span data-ttu-id="dbc96-122">출력</span><span class="sxs-lookup"><span data-stu-id="dbc96-122">OUTPUTS</span></span>

## <span data-ttu-id="dbc96-123">상속자</span><span class="sxs-lookup"><span data-stu-id="dbc96-123">NOTES</span></span>

## <span data-ttu-id="dbc96-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbc96-124">RELATED LINKS</span></span>

[<span data-ttu-id="dbc96-125">Azure Site Recovery 서비스 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dbc96-125">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


