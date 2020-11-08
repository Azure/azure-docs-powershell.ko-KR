---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 165a85f48bc39608bd636073b4b12427e0a81bf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213425"
---
# <span data-ttu-id="a9ff7-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="a9ff7-101">Get-AzProfile</span></span>

## <span data-ttu-id="a9ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ff7-103">설치 된 모듈에서 지원 되는 서비스 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9ff7-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="a9ff7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9ff7-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="a9ff7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a9ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ff7-106">설치 된 모듈에서 지원 되는 서비스 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9ff7-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="a9ff7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a9ff7-107">EXAMPLES</span></span>

### <span data-ttu-id="a9ff7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a9ff7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="a9ff7-109">KeyVault 모듈에서 지원 되는 서비스 프로필 가져오기</span><span class="sxs-lookup"><span data-stu-id="a9ff7-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="a9ff7-110">변수</span><span class="sxs-lookup"><span data-stu-id="a9ff7-110">PARAMETERS</span></span>

### <span data-ttu-id="a9ff7-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="a9ff7-111">-ListAvailable</span></span>
<span data-ttu-id="a9ff7-112">설치 된 모듈에서 지원 되는 모든 서비스 프로필 나열</span><span class="sxs-lookup"><span data-stu-id="a9ff7-112">List all service profiles supported by installed modules</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ff7-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="a9ff7-113">-ModuleName</span></span>
<span data-ttu-id="a9ff7-114">확인할 모듈의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9ff7-114">The name of the module to check</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ff7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ff7-115">CommonParameters</span></span>
<span data-ttu-id="a9ff7-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9ff7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ff7-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9ff7-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ff7-118">입력</span><span class="sxs-lookup"><span data-stu-id="a9ff7-118">INPUTS</span></span>

### <span data-ttu-id="a9ff7-119">않아야</span><span class="sxs-lookup"><span data-stu-id="a9ff7-119">None</span></span>

## <span data-ttu-id="a9ff7-120">출력</span><span class="sxs-lookup"><span data-stu-id="a9ff7-120">OUTPUTS</span></span>

### <span data-ttu-id="a9ff7-121">CommonModule. m m/. w i m/. m m m 프로필</span><span class="sxs-lookup"><span data-stu-id="a9ff7-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="a9ff7-122">상속자</span><span class="sxs-lookup"><span data-stu-id="a9ff7-122">NOTES</span></span>

## <span data-ttu-id="a9ff7-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9ff7-123">RELATED LINKS</span></span>
